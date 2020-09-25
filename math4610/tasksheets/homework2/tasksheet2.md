# SOLUTIONS FOR TASKSHEET 2

## Task 1
After deciding to write my HelloWorld program in Fortran, I wrote the following code,

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

## Task 2
I edited the main README.md file and added a description of the repository, specifically using the Google Chrome browser.

## Task 3
I created the table contents, specifically in the main README.md file of the math4610 repository, and then I used git pull to bring those updates into my local repository.

## Task 4
![Centered Difference of Approximation of the First Derivative with Taylor Series Expansions](FirstDerivative.pdf)

## Task 5
![Centered Difference of Approximation of the Second Derivative with Taylor Series Expansions](2ndDerivative.pdf)

I created the following program in Python to approximate the second derivative of cos(x) where x = 2.0. Then I created a table to display how the error changes as h decreases by an order of 10 down to 10^-16

        import math

        def main():

            exactVal = - math.cos(2.0)

            print(" The 2nd Derivative of cos(2) = ", exactVal)


            value = 2.0
            hVal = 0
            approxVal = 0


            hValList = []
            errorList = []
            diffList = []

            for i in range(0, 17):

                hVal = math.pow((1/10), i)

                approxVal = approx(value, hVal)

                hValList.append(hVal)

                errorList.append(approxVal)

                diffList.append(exactVal - approxVal)

            print("iter\t\t\th   \t \t \terror  \t\t\tdifference")
            print("----  \t ------------- \t   ------------ \t    --------------- \n")

            for j in range(0, 17):

                print("{0:2d} \t \t {1:5e} \t \t {2:5e} \t \t {3:5e}".format(j, hValList[j], errorList[j], diffList[j]))


        def approx(value, hVal):

            deriv2 = (math.cos(value + hVal) - 2*math.cos(value) + math.cos(value - hVal))/math.pow(hVal, 2)

            return deriv2


        main()

When we implement the program, it displayes the following:

         The 2nd Derivative of cos(2) =  0.4161468365471424
        iter		      h   	 	    error  	          difference
        ----  	         ------------- 	         ------------ 	        --------------- 

         0 	 	 1.000000e+00 	 	 3.826035e-01 	 	 3.354335e-02
         1 	 	 1.000000e-01 	 	 4.158002e-01 	 	 3.466735e-04
         2 	 	 1.000000e-02 	 	 4.161434e-01 	 	 3.467877e-06
         3 	 	 1.000000e-03 	 	 4.161468e-01 	 	 3.464010e-08
         4 	 	 1.000000e-04 	 	 4.161468e-01 	 	 1.954106e-08
         5 	 	 1.000000e-05 	 	 4.161471e-01 	 	 -2.802192e-07
         6 	 	 1.000000e-06 	 	 4.160006e-01 	 	 1.462692e-04
         7 	 	 1.000000e-07 	 	 4.385381e-01 	 	 -2.239126e-02
         8 	 	 1.000000e-08 	 	 1.110223e+00 	 	 -6.940762e-01
         9 	 	 1.000000e-09 	 	 5.551115e+01 	 	 -5.509500e+01
        10 	 	 1.000000e-10 	 	 0.000000e+00 	 	 4.161468e-01
        11 	 	 1.000000e-11 	 	 5.551115e+05 	 	 -5.551111e+05
        12 	 	 1.000000e-12 	 	 0.000000e+00 	 	 4.161468e-01
        13 	 	 1.000000e-13 	 	 0.000000e+00 	 	 4.161468e-01
        14 	 	 1.000000e-14 	 	 -1.665335e+12 	 	 1.665335e+12
        15 	 	 1.000000e-15 	 	 2.220446e+14 	 	 -2.220446e+14
        16 	 	 1.000000e-16 	 	 0.000000e+00 	 	 4.161468e-01


## Task 6
The examples of orders of approximation for the derivative that we have explored in class have been limited to a first order and second order approximation of the derivative. But in fact there are higher order approximations of the derivative. In fact, a formula has been generalized to find nth-order approximations for the forward, backward, and central differences. While the equations they display are difficult to write up, the article lays out how it's possible to find nth order approximations as well as how it's possible to approximate different orders (like a 2nd order approximation for the first derivative), using finite difference coefficients.

"Finite Difference." Wikipedia, en.wikipedia.org/wiki/Finite_difference#Higher-order_differences. 
