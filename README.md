# JavaScript Loose Comparison Bug

This repository demonstrates a common JavaScript bug related to loose comparison (==) and its unexpected behavior when dealing with null values in conditional statements.

## The Bug
The provided `foo` function aims to categorize numbers based on whether they are null, negative, or positive. It uses loose comparison (`==`) which can lead to unexpected behavior with null and 0:

* `null == 0` evaluates to `false` instead of the intended `true` if you want to treat null like 0

This leads to incorrect categorization of null values.

## The Solution
The solution demonstrates using strict equality (`===`) to avoid this issue. Strict equality checks both value and type, preventing the confusion between null and 0.