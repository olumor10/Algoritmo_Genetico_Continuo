# Algoritmo Genético Contínuo

## Descrição

Este projeto implementa um algoritmo genético contínuo para otimização de funções. O objetivo é encontrar o mínimo da função:

$$f(x, y) = -e^{-0.2 \sqrt{x^2 + y^2} + 3 (\cos(2x) + \sin(2y))}$$

sujeito a:

$$-5 ≤ x ≤ 5$$
$$-5 ≤ y ≤ 5$$

## Estrutura do Projeto

### Objetivo do Algoritmo

O algoritmo busca encontrar o mínimo da função de custo especificada acima.

### Fluxograma
![image](https://github.com/user-attachments/assets/5155efe4-1114-410a-ad5e-f01b00dd7008)

Fonte: Haupt; Haupt (2004)

### Função de Custo

A função de custo utilizada no algoritmo é definida como:

```python
def f_custo(x):
    return -np.exp(0.2 * np.sqrt((x[:, 0] - 1)**2 + (x[:, 1] - 1)**2) + (np.cos(2 * x[:, 0]) + np.sin(2 * x[:, 0])))
```
No entanto, a função real está comentada no início do algorito e segue abaixo:
```python
def f_custo(x):
    return -np.exp(-0.2 * np.sqrt((x[:, 0])**2 + (x[:, 1]**2)) + 3 * (np.cos(2 * x[:, 0]) + np.sin(2 * x[:, 1])))  #F15 real
```

## Referência
Haupt, R. L. and Haupt, S. E. Practical Genetic Algorithms. Wiley-Interscience, 2ª Edição. 2004.
