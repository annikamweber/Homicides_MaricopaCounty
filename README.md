README File

This project aimed to visualize homicides in Phoenix, Arizona and the 
distribution of unsolved homicides compared to solved and close cases. 

The maps are split by unsolved and solved homicides in Phoenix, Arizona. 

The data for Phoenix, Arizona did not have data on race and therefore was 
not able to color points based on race. 
The following code was used to identify that there was no race data available. 

phoenix_homicides %>%
  mutate(victim_race = fct_lump(victim_race, n = 3)) %>%
  count(victim_race)