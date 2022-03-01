# Lab 2: Michal Vida

### 2-bit comparator

1. Karnaugh maps for other two functions:

   Greater than:

   ![K-maps](images/kmap_greater.png) [//]: # (MISSING)

   Less than:

   ![K-maps](images/kmap_less.png) [//]: # (MISSING)

2. Equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

   ![Logic functions](images/comparator_min.png) [//]: # (MISSING)

### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: 07

```vhdl
    p_stimulus : process
    begin
        report "Stimulus process started" severity note;

        report "Stimulus process started" severity note;
        -- Student ID
        s_b <= "0000";
        s_a <= "0111";
        wait for 100 ns;
        assert ((s_B_greater_A = '0') and
               (s_B_equals_A  = '0') and
               (s_B_less_A    = '1'))
        report "Input combination 0000, 0111 FAILED" severity error;

        report "Stimulus process finished" severity note;
        wait;
    end process p_stimulus;
```

2. Text console screenshot during your simulation, including reports.

   ![your figure]() [//]: # (MISSING)

3. Link to your public EDA Playground example:

   [https://www.edaplayground.com/x/9K9h](https://www.edaplayground.com/x/9K9h)
