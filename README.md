# README
**WARNING: The EWS is only able to run the tests we have provided or smaller datasets, in order to run the code on the full dataset, docker memory has to be increased to 7.00 GB**

**Files and Deliverables Organisation:**

The header file for the project: Graph.h

Code for the DFS Traversal: DFS.cpp

Code for the Parsing algorithm: Parser.cpp

Code for the Dijkstra's algorithm: dijkstra.cpp

Code for the graphing algorithm: Graphing.cpp

Code that contains the tests for the algorithms for both tests and running the code on any dataset: tests/test.cpp

Input files used in the tests: data_E_test.txt, data_E_test_2.txt, data_E_test_empty.txt, data_N_test.txt, data_N_test_2.txt, data_N_test_empty.txt  

Output files used in the tests: output_test.png, output_test_path.png

Data of the chosen dataset: data_E.txt, data_N_test.txt

Drawn map of the chosen dataset: output.png

Project Proposal: Project_Proposal.md

Weekly Progress Log: Weekly_Progress_Log.md

Final Report: results.md

**Running the Code:**

First compile the program, using command line by running: make program

Tests:

- To run Tests 1 and 2, using command line type: ./program "Data Correction and Error Detection Tests"

- To run Tests 3, 4, 5 and 6, using command line type: ./program "Data Correctness Test Pt 1"

- To run Tests 7, 8 and 9, using command line type: ./program "Data Correctness Test Pt 2"

- To run Tests 10 and 11, using command line type: ./program "DFS Traversal Size Test"

- To run Tests 12, using command line type: ./program "DFS Traversal Node Order Test"

- To run Tests 13 and 14, using command line type: ./program "Graphing Algorithm Test"

- To run Test 15 type ./program "dijkstra dist test"

- To run Test 16 type ./program "dijkstra path test"

Running algorithms for general use (the target dataset is in data_E.txt (Edges) and data_N.txt (Nodes)):

To run DFS traversal on any data (prints the traversal to the console), using command line type: ./program "Run DFS". There will then be a prompt to input the following information:

- File with edge information.

- Number of edges.

- File with node information.

- Number of nodes.

To run Graphing on any data (outpust the png file with a drawing), using command line type: ./program "Graph Map". There will then be a prompt to input the following information:

- File with edge information.

- Number of edges.

- File with node information.

- Number of nodes.

- Max x coordinate.

- Max y coordinate.

- Output filename.

To run Graphing with Dijkstra's Algorithm on any data (Prints the path to the console in terms of nodes and paints the path on the map), using command line type: ./program "Graph Dijkstra Path". There will then be a prompt to input the following information:

- File with edge information.

- Number of edges.

- File with node information.

- Number of nodes.

- Max x coordinate.

- Max y coordinate.

- Output filename.

- Start node.

- End node.

To run the DFS traversal on the target dataset, that prints the first 10 elements of traversal (see results.md for more info), using command line type: ./program "DFS on the Actual Dataset Demo"

To run the Graphing on the Actual Dataset and write the result to output.png, using command line type: ./program "Graph Target Dataset"

**Description of tests:**

**Data Correction and Error Detection** (Uses "data_E_test_empty.txt" and "data_N_test_empty.txt" files as inputs)

Test 1: Checking whether the data size does not match by passing a file with less edges, than was declared for the function, so should output “error: not matching data size”.

Test 2: Test: Checking whether leaving some information fields for certain nodes empty is picked up by the algorithm. If correct should print two statements of "error: inserting empty y coordinate" and one statement of "error: not matching data size" as those entries are skipped, based on the input of data.

**Data Correctness** (Uses "data_E_test.txt" and "data_N_test.txt")

Test 3: Testing whether the information for the Start Node is correct for one of the Edges. If incorrect, the Catch test will display the value that is there instead on the left of the equals sign.

Test 4: Testing whether the information for the EdgeID is correct for one of the Edges. If incorrect, the Catch test will display the value that is there instead on the left of the equals sign.

Test 5: Testing whether the information for the End Node is correct for one of the Edges. If incorrect, the Catch test will display the value that is there instead on the left of the equals sign.

Test 6: Testing whether the information for the L2D is correct for one of the Edges. If incorrect, the Catch test will display the value that is there instead on the left of the equals sign.

Test 7: Testing whether the information for the NodeID is correct for one of the Nodes. If incorrect, the Catch test will display the value that is there instead on the left of the equals sign.

Test 8: Testing whether the information for the x coordinates is correct for one of the Nodes. If incorrect, the Catch test will display the value that is there instead on the left of the equals sign.

Test 9: Testing whether the information for the y coordinates is correct for one of the Nodes. If incorrect, the Catch test will display the value that is there instead on the left of the equals sign.

**DFS Traversal** (Uses "data_E_test.txt" and "data_N_test.txt")

Test 10: Checks for the correct number of nodes for the traversal. If incorrect, the Catch test will display the value that is there instead on the left of the equals sign.

Test 11: Checks whether any of the nodes are repeating in the traversal. If that is the case, then the function fails.

Test 12: Looking at the dataset for the test the traversal should be in the following order (By NodeIDs): 0-1-2-3-4-7-5-6. If that is not the case then the test will fail.

**Graphing Algorithm** (Uses "data_E_test_2.txt" and "data_N_test_2.txt")

Test 13: Should basically paint a "wheel" graph where there is a node in the middle of the picture, which connects to all the other nodes, which are connected in the cycle. The output is written to "output_test.png" and needs visual confirmation as a test.

Test 14: Should paint the path on top of the map done in Test 14 in blue, which is basically goes as follows: Center node - Most Southern Node - Node to immediately to the West of the most Southern Node - Center Node - Most Western Node - Node The the South of the Most Western Node - Node to the South of the Previous Node - Center Node. The output is written to "output_test_path.png" and needs visual confirmation as a test.

**Dijkstra**

Test 15: Checks that shortest distance is 7 on specified 6 node graph. 

Test 16: Checks the that the algorithm returns the correct shortest path nodes on the same adjacency matrix as above.
