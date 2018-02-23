Some of these can be asked to candidates for management / team lead type of roles as well.

 * Would you please describe your process to create a new feature and carry it to prod? What if the feature is big, it can't be isolated and it won't fit into a single sprint? (I mean it won't be possible to start and finish it in one sprint.)
 >An example answer:  
 We would code the feature in such a way that it could be enabled / disabled (after build) by using a config file.  
 Until the feature is complete we enable it only for two things:  
 1) To test the functionality added during the sprint and  
 2) To test that it does not break other parts of the software in an obvious way (by running smoke tests where we think the new code changes would affect).  
 We run all the other tests with the feature disabled (and release the sprint result with the feature disabled).  
 When the feature is complete (let's say after three sprints) we would enable the feature and do integration tests with the rest of the software and run all other tests with the feature enabled.  
 We would ship the product with the feature enabled if all tests run OK.
 * Are there people who left the company (who were in the role I am applying to) and then came back? How many people in last three years? How many in this year? Did they came back for the same position as they left?