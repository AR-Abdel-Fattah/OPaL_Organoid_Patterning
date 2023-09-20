				Organoid Patterning aLgorithm (OPaL)	

	Author: Abdel Rahman Abdel Fattah
	email: dita.roushdy@gmail.com/aabdel.fattah@cemm.at

       
       	Readme: 
      	       (OPaL_One) returns average source cell (SC) expression outputs from 
       	        a fixed set of condition inputs by using the OPaL_Single_Run function. 
	        Please keep both files (OPaL_One and OPaL_Single_Run) in the same directory.
		Input parameters in OPaL_One, Output parameters can be extracted from the MATLAB workspace

       	Inputs:
           size:       The number of elements (cells) in the domain (currently set at 46 um)
           nuc_wid:    The width of a cell's nucleus, this is used to
                       calculate domain lenght (currently set at 6 um)
           time:       The number of time steps (currently set at 10 steps)
           iterations: The number of iterations OPaL will run, this is the
                       number that will be used for averaging (analogous to number of
                       observed organoids in a culture)
           threshold:  An activation signal threshold that defines whether
                       cell remains, becomes or loses the SC identity. The higher the
                       value the more difficult it is for a cell to become an SC
                       (currnetly set at 2.36)
           induciton:  Defines the fraction of initial SCs in a domain
                       (currently set at 0.5)
           ca:         Activation signal decay constant (currently set at 0.05)
           a:          Activation signal amplitude (currently set at 1)

`      
	Outputs:
           Exp_scattering_organoids: Average scattering expression fraction
           Exp_patterning_organoids: Average patterning expression fraction
           Exp_negative_organoids: Average negative expression fraction
           Table_of_outputs: expression, SC output fraction, number of poles 
                             and position of poles for each in-silico organoid 
                             in the iteration
               Column 1: 0 = Scattered, 1 = Patterned, -1 = Negative
               Column 2: SC output fraction (between 0 and 1)
               Column 3: Number of poles detected (scattered organoids
                         still detect a pole)
              Columns 4 to 10: pole position (degs) for every pole
                               detected in the organoid