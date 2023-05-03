Download Link: https://assignmentchef.com/product/solved-cs313-data-structure-homework-2
<br>
Page 1 of 4Data Structure Homework 2 Only submit source files. Do NOT include any executables. All files should besaved in a folder and then packed into a single .zip file and be submitted viablackboard (NOT .rar or .tar.gz). The folder name (before compression) as well as the final zip file name should be“FirstName-LastName-HW2”. Ensure your code can be compiled and executed in command line (not a java IDE).Otherwise, you will NOT get any credits. In the zip file, include a text file: README.txt. Write down which problems haveyou finished. Also write down on which platform (mac, linux, window) is the codecompiled and executed. You are NOT allowed to use any native implementation of lists (ArrayList,LinkedList, etc.). Consult the instructor if you want to use any native class that is notmentioned here. This is NOT something you can finish in three days. To understand the problemitself takes quite some time. You have to start as early as possible.LLMainClass.java and the interface files (SparseM and SparseVec) should not bechanged when you submit. That is, you should not change the name/input/output ofthese major functions.Problem 1: Sparse Vector Using Linked List (5 pts) Implement the linked list sparse vector class (LLSparseVec.java) so thatLLMainClass can be executed. Nodes in the linked list are nonzero elements of the vector, sorted according to theirindices. The length of a vector is specified at construction. When an element is set to zero, the corresponding node should be removed! Implement the constructor, accessor methods, getElement, setElement,clearElement, getAllIndices, getAllValues. In otherwords, when LLMainClass iscalled using VEC argument and with a single input file, the program should be ableto run correctly and give the same output as ArrayMainClass.Page 2 of 4 Implement both the addition, subtraction and multiplication methods inLLSparseVec. The method subtraction(otherV) means the current vector minusotherV. The algorithm has to be O(m), in which m is the maximum number of nonzeroelements in a vector (length of the list). To achieve this, you cannot simply use getand set in Problem 1. Only algorithms with O(m) complexity will get credits. Thesmart-merge method in HW1 is a good place to start. But note the difference here. All operations return a new sparse vector object, storing the result. If the two vectors’ length do not match, return a null object. When LLMainClass is called using VEC argument and with multiple input files, theprogram should be able to run correctly and give the same output asArrayMainClass.Examples:Page 3 of 4Problem 2: Sparse Matrix Using Linked List (5 pts) Implement the linked list sparse matrix class (LLSparseMat.java) so thatLLMainClass can be executed with MAT argument. RowHead nodes correspond to nonzero rows. Each rowhead node stores aLLSparseVec, storing a nonzero row. It also has a pointer to the next rowhead. When a row becomes empty (no nonzero elements), the rowhead should beremoved. Implement the constructor, accessor methods: getElement, setElement, clearElement, numElements (returns number ofnon-zero elements). getRowIndices returns an array of indices of rows with nonzero elements. getOneRowColIndices returns an array of nonzero column indices of the row.Use LLSparseVec.getAllIndices(). getOneRowValues returns an array of nonzero values. UseLLSparseVec.getAllValues(). NOTE that these methods should all be linear to the number of nonzero rows ornonzero elements. Sanity check: when LLMainClass is called using MAT argument and with a singleinput file, the program should be able to run correctly and give the same output asArrayMainClass.Page 4 of 4Problem 3: Sparse Matrix Operation Linked List (5 points) Implement the addition, subtraction and multiplication methods in LLSparseM. The algorithm has to be O(m), in which m is the maximum number of nonzeroelements in a matrix. To achieve this, you cannot simply use get and set in Problem3. Only algorithms with O(m) complexity will get credits. All operations return a new sparse matrix object, storing the result. The methodsubtraction(otherM) means the current vector minus otherM. If the two matrices’ dimensions (nrows, ncols) do not match, return a null object. When LLMainClass is called using MAT argument and with multiple input files, theprogram should be able to run correctly and give the same output asArrayMainClass.Problem 4: Performance Evaluation (2 bonus points)Similar to HW1, write a report on matrix construction and operation time, comparingArray and LL implementation: 2 plots, on construction, and on operations. Each plot hastwo curves: Array implementation, and LL implementation. X-axis is the different sizesof these matrices.Samples:In Data folder, there are example inputs. At some stage, you may want to try out moreadvanced results. Use content in ManyTestCases to further test your program.