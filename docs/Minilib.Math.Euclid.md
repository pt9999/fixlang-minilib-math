# Minilib.Math.Euclid

Defined in minilib-math@0.5.1

Euclid algorithms, such as `gcd` (greatest common divisor).

`Euclid` represents a Euclidean domain, which is a Ring with following division-with-remainder.
```
forall a b, a = (a / b) * b + (a % b)
```

For details, see [Wikipedia: Euclidean domain](https://en.wikipedia.org/wiki/Euclidean_domain).

## Values

### namespace Minilib.Math.Euclid

#### _extended_euclid_inner

Type: `[a : Minilib.Math.Types::Euclid] a -> a -> (a, a, a)`

An internal function for `extended_euclid`.

#### extended_euclid

Type: `[a : Minilib.Math.Types::Euclid] a -> a -> (a, a, a)`

`extended_euclid(a,b)` performs
[Extended Euclidean algorithm](https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm).
It solves `a * x + b * y = d` where `d = gcd(a, b)`,
and returns `(x, y, d)`.

#### gcd

Type: `[a : Minilib.Math.Types::Euclid] a -> a -> a`

`gcd(a,b)` calculates the greatest common divisor of `a` and `b`.

## Types and aliases

## Traits and aliases

## Trait implementations