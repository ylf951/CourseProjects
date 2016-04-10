Tomasulo algorithm is a very important hardware technique for dynamic scheduling of instructions. This project is about the visualization of Tomasolu algorithm so that we can see how this algorithm proceeds and undertand this algorithm better.

1. Key concepts of Tomasolu algorithm  
  - Tracking dependences to allow instructions execute as soon as operands are available, avoiding RAW hazards.  
  - Register renaming to avoid WAR and WAW hazards.  
2. Three Stages of Tomasulo algorithm  
  - Issue-get instruction from head of instruction queue.  
    If reservation station free (i.e. no structual hazard), control issues instruction & sends operands (renames registers). If no data dependence, send operand value to the RS, otherwise, keep track of the function unit that produces the result.
  - Execute-operate on operands (EX)
    When both operands ready then execute; if not ready, watch Common Data Bus for result.
  - Write result-finish exection (WB)
    Write on Common Data Bus to all awaiting units; mark reservation station available.  
3. Notice
  - In this project, there are only six types of instruction (LD, SD, ADD, DIV, MUL, DIV).
4. Screenshots  
  - Initial Page
![](https://raw.githubusercontent.com/ylf951/CourseProjects/master/Tomasulo-Algorithm-Visualization/screenshots/InitialPage.png)
  - Processing
![](https://raw.githubusercontent.com/ylf951/CourseProjects/master/Tomasulo-Algorithm-Visualization/screenshots/ProcessingPage.png)
  - Finished  
![](https://raw.githubusercontent.com/ylf951/CourseProjects/master/Tomasulo-Algorithm-Visualization/screenshots/CompletedPage.png)
