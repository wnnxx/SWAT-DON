Modifications for orginal SWAT code version 664: 
1. Modparm.f (Line 969): define state variables for DON loads in subabsin and concentrations in the reach
                      (Line 970): define parameters for DON and PON reactions in the reach
2. allocate_parms.f (Line 1915-1920): allocate the size of variables for DON simulation 
                              (Line 57): modified to include 2 variables (DON and PON) for routing in array 'varoute'
                             (Line 59): modified to add 4 additional variables for organic nitrogen output in array rchdy?
3. virtual.f (Line 418-419): calculate DON and PON load using C:N ratio
                 (Line 589-590): calculate DON and PON load in subbasin for routing 
4. sim_initday.f   (Line 268-269): initialize the organic N variables to zero at the beginning of the day
5. rtout.f (Line 322-323): calculate organic N loads in outflow to downstream reach
               (Line 461-465): set daily reach output for DON and PON loads
               (Line 551-555): summarize monthly reach output for DON and PON loads
6. rchday.f (Line 191-195): for outputing daily DON and PON loads in .rch file
7. rchmon.f (Line 203-207): for outputing monthly DON and PON loads in .rch file
8. rchyr.f (Line 206-210): for outputing yearly DON and PON loads in .rch file 
9. watqual.f (Line 235): define local variables for DON and PON simulations 
                   (Line 270-271 and 292-293): calculate DON and PON concentrations 
                    (Line 326-327): calculate DON and PON initial concentrations in the reach by mixing inflow and water stored in the reach
                   (Line 822-836): update DON and PON changes after reactions in the reach
! for DON load yield output from subbasins

 virtual.f (Line 686) and submon.f (Line 83):  monthly scale DON output at subbasin

 