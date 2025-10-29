# CMPS 2200 Recitation 06
## Answers

**Name:**Viv Heurtevant



Place all written answers from `recitation-07.md` here for easier grading.



- **2)** The work for the fibonacci recurrence will be W(n) = W(n-1)+W(n-2)+1. The work on each level will be constant, however the two different subproblems will not be balanced and the leaves of the larger branch will dominate. The leave count for the fibonacci sequence is given as $/frac{\phi^n}{sqrt{5}}$, so the work is O($\phi^n$).

- **3)** The span only considers the longest branch, so S(n)= MAX(S(n-1),S(n-2))+1. This simplifies to S(n)=S(n-1)+1, which is a balanced recursion with n levels each of constant cost, meaning the span will be O(n).

- **4)** An interesting pattern with counts is that the amount of calls for each number, when sorted, becomes a descending sorting list of the (n-1) fibbonaci numbers. The only distinguishment being that the first element of the list breaks this rule and is the (n-2) fibonnaci number. This will grow rapidly for larger n, meaning we are repeating a lot of work we have already computed.

- **6)** With our top down solution, we no longer have a reccurence relation and instead a DAG that allows us to only compute each subproblem once. The total work for lookup is constant, and the depth of the problem is n, so the work is O(n). The span is also O(n) because the process is sequential, knowing the next solution requires solving the previous one first.

- **8)** The computation of each fibonacci number is constant, however because we are iterating n times to achieve the nth fibonacci number the work will be O(n). This is non-parallelizable, as each computation depends on the previous so span is also O(n).
