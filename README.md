# Exercise 1

In this exercise, you are given an input stream of data when each line of data corresponds to traffic information. Each line is encoded as a string of semi-colon (`;`) separated values and each value represents the following:

|first|second|third|fourth|
|---|---|---|---|
|source IP|destination IP|packets|bytes|

Your main task is to build a very basic firewall. This firewall has the following requirements:
1. block all trafic that is going to 192.168.30.125 that is not from the 192.168.X.X subnet;
2. block all traffic with packet count > 1000;
3. block all traffic with bytes count > 10000;
4. for every input you block, log the information in it;
5. When processing is finished, print the number of allowed bytes.

### List of tasks

Write your code on the given `main.py` file.

1. Parse the input, i.e., convert it from a string to a list of adequately typed values. E.g. `"192.168.20.12;192.168.30.125;123;86"` should become `['192.168.20.12', '192.168.30.125', 123, 86]`. *Hint: look up Python's built-in `map` function*;
2. Block the inputs according to the functional requirements of your firewall. *Hint: look up Python's built-in `filter` function*;
3. Print the sum of the allowed bytes. *Hint: look up Python's `reduce` method, which can be imported from `functools`*.

Your `main` function should have a single line of code:

```python
def main():
    firewall(input_data_stream())
```
