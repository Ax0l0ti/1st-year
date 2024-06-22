# Haskell Cheat Sheet
---
### Links:
> [[CM12006 Mathematics of Computation]]

---
#TODO Grab Docus and feed to Chat - move to correct locs
#LASTPOINT
## Polymorphism

1. **Parametric Polymorphism**
    - A function is polymorphic if it can have more than one type.
    - When the type of a function is parameterized in a type variable.

2. **Ad-hoc Polymorphism**
    - When a function is explicitly defined for multiple types using type classes.
    - The definition of (+) is different for each number type:
        - `(+) :: Int -> Int -> Int`
        - `(+) :: Integer -> Integer -> Integer`

3. **Specialisation**
    - To check for type errors, the interpreter may specialise type variables by replacing them with other types.
    - Valid type assignments for the `++` operator:
        - `(++) :: [Int] -> [Int] -> [Int]`
        - `(++) :: String -> String -> String`
        - `(++) :: [[b]] -> [[b]] -> [[b]]`
    - The most general type: `(++) :: [a] -> [a] -> [a]`

---

## Lists

1. **Building Lists**
    - Lists can be built using `[]` or `:` (cons operator).
    - Example:
        ```haskell
        countdown x
            | x <= 0 = []  -- Empty List
            | otherwise = x : countdown (x-1)  -- Header x with tail countdown (x-1)
        ```
    - `x : xs` is equivalent to `(:) x xs`.

---

## Lazy and Infinite Evaluation

1. **Lazy Evaluation**
    - Haskell only computes the required information to return an answer.

2. **Infinite Series**
    - Haskell can handle infinite series:
        - `[1..]` generates an infinite list of numbers.
        - `take [1..]` takes elements from an infinite list, e.g., `take 10 [1..]` returns the first 10 numbers.

3. **Fibonacci Series**
    - Example of generating Fibonacci numbers:
        ```haskell
        fibonacci :: [Int]
        fibonacci = makeFibonacci 1 1
            where
                makeFibonacci :: Int -> Int -> [Int]
                makeFibonacci n m = n : makeFibonacci m (n+m)
        ```
        - `take 17 fibonacci` returns the first 17 Fibonacci numbers.

---

## Higher-Order Functions

Higher-Order Functions are functions that calls other functions to compute information. This can be via the parameter call or execution call

1. **Map**
    - Applies a function to each element of a list, returning a new list with the results.
    - Example:
        ```haskell
        map :: (a -> b) -> [a] -> [b]
        map f [] = []
        map f (x:xs) = f x : map f xs
        ```

2. **Filter**
    - Filters a list based on a predicate, returning a new list containing only the elements that satisfy the predicate.
    - Example:
        ```haskell
        filter :: (a -> Bool) -> [a] -> [a]
        filter p [] = []
        filter p (x:xs) 
            | p x       = x : filter p xs
            | otherwise = filter p xs
        ```

3. **Foldr & Foldl**
    - Used for folding (reducing) a list.
    - Example using `foldr`:
        ```haskell
        sumList = foldr (+) 0 [1, 2, 3, 4]
        ```

4. **ZipWith**
    - Combines two lists with a function.
    - Example:
        ```haskell
        zipWith :: (a -> b -> c) -> [a] -> [b] -> [c]
        zipWith _ [] _ = []
        zipWith _ _ [] = []
        zipWith f (x:xs) (y:ys) = f x y : zipWith f xs ys
        ```

---

## Function Composition

1. **Compose**
    - Combines two functions to create a new function.
    - Example:
        ```haskell
        compose :: (b -> c) -> (a -> b) -> (a -> c)
        compose g f x = g (f x)
        ```

2. **List Comprehension**
    - Structure:
        ```haskell
        [ resultant output | Generation of Set(s), Requirements/Guard ]
        ```
    - Example:
        ```haskell
        [ 3*n+1 | n <- [0..10], even n]
        ```

---

## Folding

1. **Foldr**
    - Abstracts over the pattern of recursion.
    - Example:
        ```haskell
        foldr f u [] = u
        foldr f u (x:xs) = f x (foldr f u xs)
        ```
    - Using `foldr` to define `sum`, `product`, and `length`:
        ```haskell
        sum = foldr (+) 0
        product = foldr (*) 1
        length = foldr (\_ n -> n+1) 0
        ```

2. **Member Function**
    - Checks if an element is in a list using `foldr`:
        ```haskell
        member :: Eq a => a -> [a] -> Bool
        member x = foldr (\y b -> x == y || b) False
        ```

---

## Data Types

1. **Definition of Lists**
    - Lists are defined as follows:
        ```haskell
        data [a] = [] | a : [a]
        ```
    - The `data` keyword defines an inductive data type.

2. **Deriving**
    - Haskell can derive membership of some type classes by default:
        ```haskell
        data Fraction = Fraction Integer Integer deriving (Eq, Ord, Show)
        ```

---

## Trees

1. **Tree Definition**
    - A Tree is a type of graph with no loops.
    - Features:
        - Root node
        - Parent nodes with branching child nodes

2. **Types of Trees**
    - **Nth Node Trees**
    - **Binary Tree**
        - Each node has a maximum of 2 child nodes.
        - Used for computational arithmetic and data storage.

3. **Syntax of Trees**
    - Example:
        ```haskell
        data IntTree = Empty | Node Int IntTree IntTree deriving Show
        ```

4. **Inserting into a Tree**
    - Example:
        ```haskell
        insertT :: Int -> IntTree -> IntTree
        insertT x Empty = Node x Empty Empty
        insertT x (Node y left right)
            | x <= y    = Node y (insertT x left) right
            | otherwise = Node y left (insertT x right)
        ```

5. **Building an Ordered Tree from a List**
    - Example:
        ```haskell
        build :: [Int] -> IntTree
        build = foldr insertT Empty
        ```

---

## Input/Output (IO)

1. **IO Basics**
    - Placeholder for IO concepts and examples.
    - Refer to: [Input/Output Documentation](http://willem.heijltj.es/Programming_1/6-Input-output.html)

---

## Tail Recursion

1. **Tail Recursion**
    - Acts more like a while loop.
    - Example:
        ```haskell
        factorial :: Int -> Int
        factorial n = go n 1
            where
                go 0 acc = acc
                go n acc = go (n-1) (acc*n)
        ```

---


