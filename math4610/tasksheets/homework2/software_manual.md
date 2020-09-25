# Software Manual - Tasksheet 2

## Task 1
**Routine Name:** bunny

**Author:** Caleb Price

**Language:** Fortran. The code can be compiled by using the GNU Fortran compiler (gfortran)

For example:
        
        gfortran bunny.f90 
        
will produce an executable ./a.exe than can be executed. I've decided to give it a different name by doing the following:
        
        gfortran bunny.f90 -o bunny.exe 

Now I can run the program by writing the following in the terminal:

        ./bunny.exe
        
**DESCRIPTION:** This routine (bunny) will print out a statement, similar to that of a HelloWorld program for first time programmers.

**INPUT:** There are no inputs needed for this program

**OUTPUT:** This routine will return this statement
        
        It's only a bunny...
        That's no ordinary rabbit!

**USAGE:**

**IMPLEMENTATION:**

The following is the code for bunny

        PROGRAM BUNNY

                IMPLICIT NONE

                WRITE(*,*) "It's only a bunny..."
                WRITE(*,*) "That's no ordinary rabbit!"

        END PROGRAM BUNNY
        
in the file named bunny.f90. Then I compiled the code buy writing in the terminal the following:

        gfortran bunny.f90 -o bunny.exe 

which compiles the program as an executable Fortran program named bunny.exe. Now I can run the program by writing the following in the terminal:

        ./bunny.exe
        
which then displays the following:

        It's only a bunny...
        That's no ordinary rabbit!
        
**Last Modified:** September/2020      
        
## Task 5
-I didn't write a software manual for this program since it was not required for the homework
