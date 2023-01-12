# ExamsScheduler
Finding the optimal final exams schedule for credit hours system

first we have to find for each exam day 3 courses that can be examined and for this there is only one criteria which is that a student can't have two exams
at the same day ie course1.students $\bigcap$ course2.students $\bigcap$  course3.students = $\phi$
and then we do the same for only two courses and then finally we have one courses that can't paired with anything else

we iterate the previous step and choose the minimum number of days as it will yield more number of gap days between each exam 

finally that we have the minimum number of examination days we have to find the best suitable order for most student
we define that the best schedule is that in which have the biggest dispersion 

we measure the dispersion with median absolute deviation rather than standard deviation or other similar measurements as it's more robust and more resilient to outliers. this is critical because a schedule that have a gap of 9 days and then all other exams are consecutive would be misleadingly good choice
 
$MAD=median(|x_i - median(x)|$

