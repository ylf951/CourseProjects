Tomasolu algorithm is a very important hardware technique for dynamic scheduling of instructions.

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
