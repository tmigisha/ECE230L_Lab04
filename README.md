# Lab 04 - SOP/POS and KMaps

In this lab, you’ve learned how to apply KMaps, Sum Of Products and Products of
sums to simplify digital logic equations. Then, you’ve proven out that they work
using an implemented design on your Basys3 boards.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Summary

Summarize your learnings from the lab here.
* Learned how to find SOP and POS from a KMap of a truth table.
* Learned how to make an optimal Boolean equation by overlapping groups in KMaps.
* Learned how to code Boolean equations in Verilog.
* Learned how to view the schematics (circuit diagram) of our modules.
  
## Lab Questions

### Why are the groups of 1’s (or 0’s) that we select in the KMap able to go across edges?
* Because only one variable is changing from one edge to another. 
### Why are the names Sum of Products and Products of Sums?
* For Sum of Products, we OR all the minterms (AND equations).
* For Product of Sums, we AND all the maxterms (OR equations)
### Open the test.v file – how are we able to check that the signals match using XOR?
if (led[0] ^ led[1] != 0) begin
            $display("Minterm output does not match");
            $finish;
        end
* The XOR takes in the output from the naive and minterm modules.
* It is checking whether the two outputs match. If they don't match, the condition will output 1, which will throw the error message.
