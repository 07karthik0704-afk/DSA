# Ruby DSA Notes — Arrays (Two Sum Preparation)

## 1. What is an Array?

An array stores multiple values in a single variable.

```ruby
nums = [2, 7, 11, 15]
```

Each element has an index, starting from `0`.

| Index | Value |
|---:|---:|
| 0 | 2 |
| 1 | 7 |
| 2 | 11 |
| 3 | 15 |

## 2. Accessing Array Elements

```ruby
nums[0] # 2
nums[1] # 7
nums[2] # 11
nums[3] # 15
```

**Important:** Index and value are different.

- Index → position of an element.
- Value → actual number stored at that position.

For Two Sum, we return indices, not values.

## 3. Array Length

```ruby
nums.length
```

Output:

```text
4
```

Useful for determining how many elements exist and controlling loops.

## 4. Array Traversal

Traversal means visiting each element in an array.

### Using a `for` loop

```ruby
for i in 0...nums.length
  puts nums[i]
end
```

Here:

- `i` represents the index.
- `nums[i]` represents the value.
- `0...nums.length` iterates through valid indices.

### Using `each`

```ruby
nums.each do |number|
  puts number
end
```

`each` visits every element directly.

## 5. Array Traversal with Indices

```ruby
for i in 0...nums.length
  puts "Index: #{i}, Value: #{nums[i]}"
end
```

This is useful when a problem requires returning indices.

## 6. Conditions Inside Loops

```ruby
if nums[i] > 10
  puts nums[i]
end
```

Conditions allow us to check whether an element satisfies a requirement.

For Two Sum:

```ruby
if nums[i] + nums[j] == target
```

This checks whether two numbers equal the target when added.

## 7. Nested Loops

A nested loop is a loop inside another loop.

```ruby
for i in 0...nums.length
  for j in (i + 1)...nums.length
    puts "#{nums[i]} + #{nums[j]}"
  end
end
```

### Why `j = i + 1`?

- Avoids pairing an element with itself.
- Avoids checking the same pair twice.
- Useful for brute-force Two Sum.

## 8. Returning Array Indices

```ruby
return [i, j]
```

This returns the indices of the two elements.

Example:

```ruby
nums = [2, 7, 11, 15]
```

If `i = 0` and `j = 1`:

```ruby
return [0, 1]
```

Not:

```ruby
return [2, 7]
```

Because the problem asks for indices.

## 9. Time Complexity of Array Loops

| Operation | Time Complexity |
|---|---|
| Access `nums[i]` | O(1) |
| Traverse array | O(n) |
| Single loop | O(n) |
| Nested loops | O(n²) |

Your brute-force Two Sum uses nested loops, so its time complexity is O(n²).

## 10. Complete Array Concepts Needed for Two Sum

- [x] Array declaration
- [x] Array indexing
- [x] Array length
- [x] Array traversal
- [x] Index-based loops
- [x] Conditions inside loops
- [x] Nested loops
- [x] Returning indices
- [x] Understanding O(n) and O(n²)

**Array fundamentals required for Two Sum are now covered.**

