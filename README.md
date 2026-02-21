# DEEP-LEARNING-COMCEPTOS 1 semana
[Untitled1.ipynb](https://github.com/user-attachments/files/25455257/Untitled1.ipynb)
{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": []
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "code",
      "execution_count": 19,
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "xE8zNXPOmAJL",
        "outputId": "64118601-e953-4bbd-baa9-b9af41339ca4"
      },
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Entrada=(0,0) z=-1.5 salida=0\n",
            "Entrada=(0,1) z=-0.5 salida=0\n",
            "Entrada=(1,0) z=-0.5 salida=0\n",
            "Entrada=(1,1) z=0.5 salida=1\n"
          ]
        }
      ],
      "source": [
        "import numpy as np\n",
        "def step(z):\n",
        "    return 1 if z >= 0 else 0\n",
        "def neurona(x1, x2, w1, w2, b):\n",
        "    z = x1*w1 + x2*w2 + b\n",
        "    y = step(z)\n",
        "    return z, y\n",
        "# Valores base\n",
        "w1, w2, b = 1, 1, -1.5 # intenta parecerse a una compuerta AND\n",
        "casos = [(0,0),(0,1),(1,0),(1,1)]\n",
        "for x1, x2 in casos:\n",
        "    z, y = neurona(x1, x2, w1, w2, b)\n",
        "    print(f\"Entrada=({x1},{x2}) z={z:.1f} salida={y}\")"
      ]
    },
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "46fd07ac"
      },
      "source": [
        "### Understanding the 'AND' Gate Behavior with Bias `b`\n",
        "\n",
        "The `neurona` function with `w1=1` and `w2=1` simulates a simple perceptron. For it to behave like an AND gate, the following conditions must be met for `z = x1*w1 + x2*w2 + b`:\n",
        "\n",
        "*   **Input (0,0):** `z = 0*1 + 0*1 + b = b`. We need `z < 0` so `step(z)` is 0. Thus, `b < 0`.\n",
        "*   **Input (0,1):** `z = 0*1 + 1*1 + b = 1 + b`. We need `z < 0` so `step(z)` is 0. Thus, `1 + b < 0` which means `b < -1`.\n",
        "*   **Input (1,0):** `z = 1*1 + 0*1 + b = 1 + b`. We need `z < 0` so `step(z)` is 0. Thus, `1 + b < 0` which means `b < -1`.\n",
        "*   **Input (1,1):** `z = 1*1 + 1*1 + b = 2 + b`. We need `z >= 0` so `step(z)` is 1. Thus, `2 + b >= 0` which means `b >= -2`.\n",
        "\n",
        "Combining these conditions, `b` must be in the range **`-2 <= b < -1`**. The current value `b = -1.5` is within this range, meaning the neuron is already correctly simulating an AND gate.\n",
        "\n",
        "Let's test some `b` values."
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "8183cdb7",
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "outputId": "ef3194f7-f8e2-4311-8029-fde1b34c098a"
      },
      "source": [
        "# Test with the current b value (which is correct for AND gate)\n",
        "print(\"\\n--- Testing with b = -1.5 (AND gate behavior) ---\")\n",
        "w1, w2, b_and = 1, 1, -1.5\n",
        "for x1, x2 in casos:\n",
        "    z, y = neurona(x1, x2, w1, w2, b_and)\n",
        "    print(f\"Entrada=({x1},{x2}) z={z:.1f} salida={y}\")\n",
        "\n",
        "# Test with a b value outside the range (e.g., b = -0.5), which would act like an OR gate\n",
        "print(\"\\n--- Testing with b = -0.5 (OR gate behavior) ---\")\n",
        "w1, w2, b_or = 1, 1, -0.5\n",
        "for x1, x2 in casos:\n",
        "    z, y = neurona(x1, x2, w1, w2, b_or)\n",
        "    print(f\"Entrada=({x1},{x2}) z={z:.1f} salida={y}\")\n",
        "\n",
        "# Test with another b value outside the range (e.g., b = -2.5), which would output 0 for (1,1)\n",
        "print(\"\\n--- Testing with b = -2.5 (Always 0 for (1,1)) ---\")\n",
        "w1, w2, b_fail = 1, 1, -2.5\n",
        "for x1, x2 in casos:\n",
        "    z, y = neurona(x1, x2, w1, w2, b_fail)\n",
        "    print(f\"Entrada=({x1},{x2}) z={z:.1f} salida={y}\")"
      ],
      "execution_count": 12,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "\n",
            "--- Testing with b = -1.5 (AND gate behavior) ---\n",
            "Entrada=(0,0) z=-1.5 salida=0\n",
            "Entrada=(0,1) z=-0.5 salida=0\n",
            "Entrada=(1,0) z=-0.5 salida=0\n",
            "Entrada=(1,1) z=0.5 salida=1\n",
            "\n",
            "--- Testing with b = -0.5 (OR gate behavior) ---\n",
            "Entrada=(0,0) z=-0.5 salida=0\n",
            "Entrada=(0,1) z=0.5 salida=1\n",
            "Entrada=(1,0) z=0.5 salida=1\n",
            "Entrada=(1,1) z=1.5 salida=1\n",
            "\n",
            "--- Testing with b = -2.5 (Always 0 for (1,1)) ---\n",
            "Entrada=(0,0) z=-2.5 salida=0\n",
            "Entrada=(0,1) z=-1.5 salida=0\n",
            "Entrada=(1,0) z=-1.5 salida=0\n",
            "Entrada=(1,1) z=-0.5 salida=0\n"
          ]
        }
      ]
    }
  ]
}
