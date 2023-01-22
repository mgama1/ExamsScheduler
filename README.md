# ExamsScheduler
Finding the optimal final exams schedule for credit hours system

first we have to find for each exam day, 3 courses that can be examined and for this there is only one criteria which is that - $\ \bigcap\limits_{i=1}^{n}course_{i}.students$ is mutually exclusive. ie course1.students $\bigcap$ course2.students $\bigcap$  course3.students = $\phi$
and then we do the same for only two courses and then finally we have one courses that can't paired with anything else

we iterate the previous step and choose the minimum number of days as it will yield more number of gap days between each exam 

finally that we have the minimum number of examination days we have to find the best suitable order for most student
we define that the best schedule is that in which have the biggest dispersion 

we measure the dispersion with median absolute deviation rather than standard deviation or other similar measurements as it's more robust and more resilient to outliers. this is critical because a schedule that have a gap of 9 days and then all other exams are consecutive would be misleadingly good choice
 
$MAD=median(|x_i - median(x)|$






.
given the enrolled courses this semester the program found that this is the best possible outcome 
it's worthy to note that the coordinator could only narrow it down to 16 days while the programm found a 14 days solution

|    | course1             | course2               | course3                    |
|---:|:--------------------|:----------------------|:---------------------------|
|  0 | TechnicalWriting    | -                     | -                          |
|  1 | Electronics1        | InudstrialElectronics | -                          |
|  2 | MachineDesign2      | FundOfMangement       | -                          |
|  3 | EngineeringDrawing  | Signal                | NumericalControl           |
|  4 | Calc3               | Physics               | Microcontroller            |
|  5 | CSAndProgramming    | Ethics                | AVS                        |
|  6 | Logic               | -                     | -                          |
|  7 | calc1               | Robotics              | Mechatronics1              |
|  8 | FundOfManuf         | DigitalControl        | MechanicsAndThermodynamics |
|  9 | Fluid               | -                     | -                          |
| 10 | SensorsAndActuators | Fields                | -                          |
| 11 | Vibration           | accounting            | -                          |
| 12 | Mechanics1          | PLC                   | Control1                   |
| 13 | LinearAlgebra       | ManufSystemAutomation | Thermodynamics             |

