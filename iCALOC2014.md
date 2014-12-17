# The iCALOC2014

## Assignment
Intelliplan is developing a new candidate search. The candidates are anonymised and assigned skills according to a given pattern.
Your task is to given a specific search criteria sort and find any candidate that matches.

## The input
Input will be given on **standard in**.

The input is separated in two parts. **Data** and **Examples**.
Each part identified by a header with either *Data* or *Exampels* preceded with a hash mark *( # )*.

#### Data
A candidate is identified with a positive integer *n (0 <= n <= 10 000)* followed by a colon *( : )*.
Following that, a comma separated list of *skills* ranging from **A to Z**.

#### Examples
Examples are given as sets on the form {A,B,..., Z} or {A},{B},...{Z} or any combination of that.

**AND** is denoted within a set such as {A,B}. Thus that can be read: Any candidate that has both skill A **and** B.

**OR** is denoted outside a set such as {A},{B}. Thus that can be read: Any candidate that has both skill A **or** B.


## The output
The output should be presented on the form:

{EXAMPLE}: [comma separated list of candidate identifiers]

If no candidate fulfils the criteria, the list of candidates should be substituted by the text: *None apply*.

## Example

### input:
```
# Data
1: A,B,C
2: B,C
3: A,B
4: C,D

# Examples
{A,B}
{B},{C}
{E}
```

### output:
```
{A,B}: 1,3
{B}||{C}: 1,2,3,4
{E}: None apply
```
