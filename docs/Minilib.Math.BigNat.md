# Minilib.Math.BigNat

Defined in minilib-math@0.5.1

Arbitrary-precision natural number. This is internal module of BigInt.

## Values

### namespace Minilib.Math.BigNat

#### _add

Type: `Std::Array Std::U32 -> Std::Array Std::U32 -> Std::Array Std::U32`

Calculates `a0 + a1`.

#### _add_u32_with_offset1

Type: `Std::Array Std::U32 -> Std::U32 -> Std::I64 -> Std::Array Std::U32`

`_add_u32_with_offset1(a0, a1, offset1)` calculates `a0 + a1 * pow(_base, offset1)`.

#### _add_u64_with_exp

Type: `Std::Array Std::U32 -> Std::U64 -> Std::U64 -> Std::Array Std::U32`

`_add_u64_with_exp(a, bm, be)` calculates `a + bm * pow(2, be)`.

#### _add_with_offset1

Type: `Std::Array Std::U32 -> (Std::Array Std::U32, Std::I64) -> Std::Array Std::U32`

Calculates `a0 + a1 * pow(_base, offset1)`.

#### _append_last_zeros

Type: `Std::I64 -> Std::Array Std::U32 -> Std::Array Std::U32`

Appends trailing zeros until the size of the array is at least the specified size.

#### _approx_with_exp

Type: `Std::I64 -> Std::Array Std::U32 -> (Std::U64, Std::I64)`

Approximate BigNat `a` as `m * 2^e`.
`m` is the mantissa and its type is U64.
`e` is the expopnent and its type is I64.
If the bitlength of `a` is smaller or equal to `m_bitlen`, returns `(a._to_u64, 0)`.
It should be hold that `m * e^2 <= a < (m+1) * e^2`.

#### _base

Type: `Std::U64`

The base of BigNat. It must be power of 2.

#### _bit_length

Type: `Std::Array Std::U32 -> Std::U64`

Returns the bit length of `a`, ie. one plus the bit position of most significant `1`.
Returns 0 if `a` is zero.

#### _cmp

Type: `(Std::Array Std::U32, Std::I64) -> (Std::Array Std::U32, Std::I64) -> Std::I64`

Calculates `sign(a0 * _base ^ offset0 - a1 * _base ^ offset1)`.

#### _convert_borrow_to_sign

Type: `(Std::Array Std::U32, Std::U64) -> (Std::Array Std::U32, Std::I64)`

Converts a result of a borrowed subtraction to a signed subtraction.

#### _divmod

Type: `Std::Array Std::U32 -> Std::Array Std::U32 -> (Std::Array Std::U32, Std::Array Std::U32)`

Calculates `(a0 / a1, a0 % a1)`.
Aborts if any error occured.

#### _divmod_base

Type: `Std::U64 -> (Std::U64, Std::U64)`

divmod by _base.

#### _divmod_by_power_of_two

Type: `Std::Array Std::U32 -> Std::U64 -> (Std::Array Std::U32, Std::Array Std::U32)`

Calculates `(a0 / 2 ^ exp, a0 % 2 ^ exp)`.
Aborts if any error occured.

#### _divmod_by_two

Type: `Std::Array Std::U32 -> (Std::Array Std::U32, Std::Array Std::U32)`

Calculates `(a0 / 2, a0 % 2)`.
Aborts if any error occured.

#### _divmod_log2_base

Type: `Std::U64 -> (Std::U64, Std::U64)`

divmod by _log2_base.

#### _divmod_u32

Type: `Std::Array Std::U32 -> Std::U32 -> (Std::Array Std::U32, Std::U32)`

Calculates `(a0 / d1, a0 % d1)`.

#### _dummy

Type: `()`

#### _from_string_inner

Type: `Std::Array Std::U8 -> Std::I64 -> Std::Array Std::U32 -> Std::Result Std::ErrMsg (Std::Array Std::U32)`

FromString of BigNat.

#### _from_u64

Type: `Std::U64 -> Std::Array Std::U32`

Converts U64 to BigNat.

#### _generate_bignat

Type: `Std::I64 -> Random::Random -> (Random::Random, Std::Array Std::U32)`

#### _generate_bignat_range

Type: `Std::Array Std::U32 -> Std::Array Std::U32 -> Random::Random -> (Random::Random, Std::Array Std::U32)`

#### _is_zero

Type: `Std::Array Std::U32 -> Std::Bool`

Returns true if BigNat is zero.

#### _log2_base

Type: `Std::U64`

log2 of base. It must be power of 2 and `0 <= _log2_base <= 32`.

#### _log2_log2_base

Type: `Std::U64`

log2(log2(base)). It must be `0 <= _log2_log2_base <= 5`.

#### _mul

Type: `Std::Array Std::U32 -> Std::Array Std::U32 -> Std::Array Std::U32`

Calculates `a0 * a1`.

#### _mul_u32

Type: `Std::U32 -> Std::Array Std::U32 -> Std::Array Std::U32`

Calculates `d0 * a1`.

#### _neg

Type: `Std::Array Std::U32 -> Std::Array Std::U32`

Treats `a` as a negative number in two's complement representation and reverses its sign.

#### _one

Type: `Std::Array Std::U32`

1 in BigNat.

#### _pow_by_U64

Type: `Std::Array Std::U32 -> Std::U64 -> Std::Array Std::U32`

Calculates `a^n`.

#### _remove_last_zeros

Type: `Std::Array Std::U32 -> Std::Array Std::U32`

Removes trailing zeros.

#### _shift_left

Type: `Std::U64 -> Std::Array Std::U32 -> Std::Array Std::U32`

#### _shift_right

Type: `Std::U64 -> Std::Array Std::U32 -> Std::Array Std::U32`

#### _signed_sub_with_offset

Type: `(Std::Array Std::U32, Std::I64) -> (Std::Array Std::U32, Std::I64) -> ((Std::Array Std::U32, Std::I64), Std::I64)`

Calculates `a0 * pow(_base, offset0) - a1 * pow(_base, offset1)`.
returns the result and the sign.

#### _sub

Type: `Std::Array Std::U32 -> Std::Array Std::U32 -> Std::Array Std::U32`

Calculates `a0 - a1`.
Aborts if the result is negative.

#### _sub_u32_with_offset

Type: `Std::Array Std::U32 -> Std::U32 -> Std::I64 -> (Std::Array Std::U32, Std::U64)`

`_sub_u32_with_offset(a, b, b_offset)` calculates `a - b * pow(_base, b_offset)`.
returns the result and the borrow.

#### _sub_u64_with_exp

Type: `Std::Array Std::U32 -> Std::U64 -> Std::U64 -> (Std::Array Std::U32, Std::U64)`

`_sub_u64_with_exp(a, bm, be)` calculates `a - bm * pow(2, be)`.
Returns the result and the borrow.

#### _sub_with_exp_mul

Type: `Std::Array Std::U32 -> Std::Array Std::U32 -> Std::U64 -> Std::U64 -> (Std::Array Std::U32, Std::U64)`

`_sub_with_exp_mul(a, b, qm, qe)` calculates `a - b * qm * pow(2, qe)`.
Returns the result and the borrow.

#### _sub_with_offset_mul

Type: `Std::Array Std::U32 -> Std::Array Std::U32 -> Std::U32 -> Std::I64 -> (Std::Array Std::U32, Std::U64)`

`_sub_with_offset_mul(a, b, q, b_offset)` calculates `a - b * q * pow(_base, b_offset)`.
Returns the result and the borrow.

#### _to_string

Type: `Std::Array Std::U32 -> Std::String`

ToString of BigNat.

#### _to_string_hex

Type: `Std::Array Std::U32 -> Std::String`

#### _to_string_inner

Type: `Std::Array Std::U32 -> Std::Iterator::DynIterator Std::U8 -> Std::Iterator::DynIterator Std::U8`

#### _to_u64

Type: `Std::Array Std::U32 -> Std::U64`

Converts BigNat to U64. If overflow, it produces unexpected result.

#### _two

Type: `Std::Array Std::U32`

2 in BigNat.

#### _zero

Type: `Std::Array Std::U32`

0 in BigNat.

## Types and aliases

## Traits and aliases

## Trait implementations