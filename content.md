# Ruby Numbers

Go beyond basic counting and unlock the full power of Ruby's numeric classes.

## Goal

In this lesson, you'll learn how to work with numbers in Ruby: integers, floats, simple math operations, type conversions, and common numeric methods.

## 1. What Are Numbers in Ruby?

In Ruby, numbers are objects, just like strings. You can call methods on them directly.

```ruby
# Integer
pp 5.class

# Float
pp 3.14.class
```
{: .repl }

Ruby has several numeric classes, but for beginners the most important are:

- [Integer](https://ruby-doc.org/3.4.1/Integer.html) — whole numbers like 42 or -7.
- [Float](https://ruby-doc.org/3.4.1/Float.html) — decimal numbers like 3.14 or -0.5.
- Other types ([Rational](https://ruby-doc.org/3.4.1/Rational.html), [Complex](https://ruby-doc.org/3.4.1/Complex.html), [BigDecimal](https://ruby-doc.org/3.4.1/gems/bigdecimal/BigDecimal.html)) are useful later but not essential at the start.

## 2. Integer vs Float Division

Division behaves differently depending on whether you use integers or floats.

```ruby
# 2 (integer division)
pp 5 / 2

# 2.5 (float division)
pp 5 / 2.0
```
{: .repl }

<aside class="warning">
  <strong>Gotcha:</strong> Beginners are often surprised when <code>5 / 2</code> gives <code>2</code> instead of <code>2.5</code>. Use a float if you want a decimal answer.
</aside>

## 3. Converting Between Types

You can convert between integers, floats, and strings:

```ruby
# 42
pp "42".to_i

# 3.14
pp "3.14".to_f

# 5.0
pp 5.to_f

# 3
pp 3.7.to_i
```
{: .repl }

## 4. Common Math Operations

Ruby supports all the usual operators:

```ruby
# 10
pp 7 + 3

# 4
pp 7 - 3

# 21
pp 7 * 3

# 2
pp 7 / 3

# 1 (remainder)
pp 7 % 3

# 8 (2 to the 3rd power)
pp 2**3
```
{: .repl }

### Division and Remainder

Ruby uses two operators for division:

- `/` — gives the quotient (the "whole number" part of division if both operands are integers).
- `%` — gives the remainder (what's left over after dividing).

```ruby
# 2
pp 7 / 3

# 1
pp 7 % 3
```
{: .repl }

Think of it like dividing snacks among friends:

- If you have 7 cookies and 3 friends, each gets 2 cookies (7 / 3).
- There will be 1 cookie left over (7 % 3).

<aside class="tip">
  The <code>%</code> operator is often called <em>modulo</em>. It's super useful for problems like checking if a number is even (<code>n % 2 == 0</code>).
</aside>

## 5. Useful Numeric Methods

Numbers come with handy methods:

```ruby
# 7 (absolute value)
pp -7.abs

# 6
pp 5.next

# 2 (greatest common divisor)
pp 10.gcd(6)

# random number from 0–9
pp rand(10)
```
{: .repl }

## 6. Predicate Methods (?)

Many number methods end with a question mark. These are predicates, they return true or false.

```ruby
# false
pp 5.even?

# false
pp 8.odd?

# true
pp 0.zero?
```
{: .repl }

## 7. Float Quirks

Because floats use binary under the hood, they sometimes give rounding errors.

```ruby
# 0.30000000000000004
pp 0.1 + 0.2
```
{: .repl }

<aside class="tip">
  Floats are fine anytime tiny rounding differences don't matter. In cases you need exact decimal answers (eg financial apps), Ruby provides [BigDecimal](https://ruby-doc.org/3.4.1/gems/bigdecimal/BigDecimal.html) for precise decimal math or simply use Integers in the smallest unit (eg 101 cents for $1.01).
</aside>

## Wrap-Up

You've learned:

- The difference between integers and floats
- How division changes with numeric types
- How to convert between strings, integers, and floats
- Basic math operators and useful numeric methods
- Predicate methods like even? and zero?
- Float quirks and when to use BigDecimal or Integer

## Quiz

- What is the result of 7 / 2 in Ruby?
- 3.5
  - Not correct. That would be float division.
- 2
  - Correct! Integer division truncates the result.
- 2.5
  - Not correct. You'd need a float for that.
{: .choose_best #int_div title="Integer Division" answer="2"}

- Which of the following are true about Ruby numbers?
- 5.next returns 6.
  - Correct!
- Floats are always exact.
  - Incorrect. Floats can have rounding errors.
- "10".to_i converts a string to an integer.
  - Correct!
- 7 % 3 equals 3.
  - Incorrect. The remainder is 1.
{: .choose_all #num_basics title="Numeric Basics" answer="[1,3]"}

## Project: Number

In this project, you will write Ruby programs that leverage these string methods. This project includes automated tests, so click this link to get started <https://github.com/dpi-tta-projects/ruby-numeric/fork>, fork the repository and create a codespace.

<aside class="warning">
  In order to get credit for completing this project you'll need to open the assignment link from canvas to generate an access token.
</aside>

## References

- Ruby Docs: [Integer](https://ruby-doc.org/3.4.1/Integer.html)
- Ruby Docs: [Float](https://ruby-doc.org/3.4.1/Float.html)
- Ruby Docs: [Float](https://ruby-doc.org/3.4.1/Numeric.html)
