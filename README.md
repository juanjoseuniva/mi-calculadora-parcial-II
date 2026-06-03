# Calculadora CI - Parcial PHP

Calculadora en PHP con pruebas unitarias (PHPUnit) e integración continua con GitHub Actions.
Ciclo TDD: Rojo → Verde → Rojo → Verde.

## Badge

[![PHP CI](https://github.com/juanjoseuniva/mi-calculadora-parcial-II/actions/workflows/php-ci.yml/badge.svg)](https://github.com/juanjoseuniva/mi-calculadora-parcial-II/actions)

## Estructura del proyecto

```
PARCIAL/
├── src/
│   └── Calculadora.php          # Clase con operaciones aritméticas
├── tests/
│   └── CalculadoraTest.php      # Pruebas unitarias con PHPUnit
├── .github/
│   └── workflows/
│       └── php-ci.yml           # Workflow de integración continua
├── composer.json                 # Dependencias y autoload
└── README.md                     # Este archivo
```

## Funcionalidades implementadas

| Operación | Método | Descripción |
|-----------|--------|-------------|
| Suma | `sumar($a, $b)` | Retorna `$a + $b` |
| Resta | `restar($a, $b)` | Retorna `$a - $b` |
| Multiplicación | `multiplicar($a, $b)` | Retorna `$a * $b` |
| División | `dividir($a, $b)` | Retorna `$a / $b`. Lanza `\InvalidArgumentException` si `$b == 0` |

## Pruebas unitarias

| Prueba | Descripción | Resultado esperado |
|--------|-------------|-------------------|
| `testSuma()` | `sumar(2, 3)` debe ser `5` | ✅ Pasa |
| `testResta()` | `restar(4, 3)` debe ser `1` | ✅ Pasa |
| `testMultiplicacion()` | `multiplicar(4, 3)` debe ser `12` | ✅ Pasa |
| `testDivision()` | `dividir(6, 3)` debe ser `2` | ✅ Pasa |
| `testDivisionPorCeroLanzaExcepcion()` | `dividir(5, 0)` debe lanzar `\InvalidArgumentException` | ✅ Pasa |

## Ciclo TDD aplicado

1. **Estructura inicial** — Suma, resta y multiplicación funcionando
2. **testDivision()** → Falla (rojo) porque `dividir()` retorna `0`
3. **Implementar dividir()** → Pasa (verde)
4. **testDivisionPorCeroLanzaExcepcion()** → Falla (rojo) porque no hay validación
5. **Lanzar excepción al dividir por cero** → Pasa (verde)
6. **README con badge y documentación**

## Tecnologías

- PHP 8.2
- PHPUnit 10
- Composer
- GitHub Actions

## URL del repositorio

https://github.com/juanjoseuniva/mi-calculadora-parcial-II.git

# Integrantes

Juan José Campo López

# Links de los commits

https://github.com/juanjoseuniva/mi-calculadora-parcial-II/commits/main/
