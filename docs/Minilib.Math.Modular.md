# Minilib.Math.Modular

Defined in minilib-math@0.5.1

This is an arithmetic with a modulus (modulo), for example `2 * 5 = 10 = 3 (mod 7)`.

For details, see [Wikipedia: Modular Arithmetic](https://en.wikipedia.org/wiki/Modular_arithmetic).

## Values

### namespace Minilib.Math.Modular

#### _get_modulus

Type: `[a : Minilib.Math.Types::Euclid] Minilib.Math.Modular::Modular a -> Minilib.Math.Modular::Modular a -> a`

Returns modulus of either `x` or `y`.

#### make

Type: `[a : Minilib.Math.Types::Euclid] a -> a -> Minilib.Math.Modular::Modular a`

`Modular::make(v, m)` creates `v modulo m`.
It is an equivalence class of a quotient ring `Z/mZ`.

#### modulo

Type: `[a : Minilib.Math.Types::Euclid] a -> a -> Minilib.Math.Modular::Modular a`

Synonym for `Modular::make`.

#### nonneg

Type: `[a : Minilib.Math.Types::Euclid, a : Std::LessThan] Minilib.Math.Modular::Modular a -> Minilib.Math.Modular::Modular a`

`x.nonneg` changes `@value` with a equivalent non-negative value.
For example, `modulo(-1, 3)` will be changed to `modulo(2,3)`
because `-1 == 2 mod 3`.

## Types and aliases

### namespace Minilib.Math.Modular

#### Modular

Defined as: `type Modular a = unbox struct { ...fields... }`

A type that performs Modular Arithmetic.

##### field `value`

Type: `a`

##### field `modulus`

Type: `a`

## Traits and aliases

## Trait implementations

### impl `[a : Minilib.Math.Types::Euclid] Minilib.Math.Modular::Modular a : Minilib.Math.Types::One`

### impl `[a : Minilib.Math.Types::Euclid] Minilib.Math.Modular::Modular a : Std::Add`

### impl `[a : Minilib.Math.Types::Euclid] Minilib.Math.Modular::Modular a : Std::Div`

### impl `[a : Minilib.Math.Types::Euclid] Minilib.Math.Modular::Modular a : Std::Eq`

### impl `[a : Minilib.Math.Types::Euclid] Minilib.Math.Modular::Modular a : Std::Mul`

### impl `[a : Minilib.Math.Types::Euclid] Minilib.Math.Modular::Modular a : Std::Neg`

### impl `[a : Minilib.Math.Types::Euclid] Minilib.Math.Modular::Modular a : Std::Sub`

### impl `[a : Std::ToString] Minilib.Math.Modular::Modular a : Std::ToString`

### impl `[a : Minilib.Math.Types::Euclid] Minilib.Math.Modular::Modular a : Std::Zero`