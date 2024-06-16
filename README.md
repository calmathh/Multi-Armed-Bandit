There are 3 files in this this GitHub which is how I've tried to interpret a multiarmed Bandit Problem as of Seasons of Code'24-Assignment-1,WnCC
Essentially the Problem has 5 buttons -each with the 5 different ditributions(Gaussian,Binomial,Poisson,Exponential and a random function which chooses any one distribution out of the rest 4)
so there's 100 timesteps which make an episode and the rewards at the end of each episode are plotted using Matplotlib run for 1000 episodes
FILE-EXPLOIT EACH
So first of to get a feel of explore vs exploit i tried using the first 5 episodes(each episode just clicking one button to get all datapoints of rewards by clicking that button)
Then plotted each episodes'(essentially each button's rewards over 100 time steps on a graph along with histogram of results obtained to get a feel of the data)
Further updated the mean of the button rewards data on expected_avgerage array which will be used in the later steps
Rest of the 995 episodes i just used to exploit the button which has the maximum average and woah! yes that did give a stable(kinda) output after a linear increase of rewards from the initial like 5 exploration steps
FILE-MULTI BANDIT
here i used epsilon greedy algorithm essentially entered by the user epsilon keeps decaying inorder to achieve optimal high reward by the end,epsilon times of 1000*100 times it explores and rest it exploits which is implemented by considering a float betwwen [0,1] and epsilon and if epsilon is lower than that random float it explores, so lower epsilon more it exploits
considering the distributions in the problem statement
But due to various types of distributions especially binomial whcih has a wide range of mean values considering the high variation in the rewards the result of the graph was that the rewards we stagnating at a point lower than the max it attained after 900 episodes which does not serve the purpose
This could also be because the algothrim involves so many choices which are random and distributions also are high risk(esp binomial)
so i tried it on a similar gaussian kinda distributins filr
FILE-SIMILAR DISTRIBUTIONS GREEDY ALGO MULTI-BANDIT
used the same algorithm but changed the buttons to all being gaussian distributions with different means,to check if algorithm works on such a function
OLA! yes it does it perfectly is linear and later stagnates with very less noise with lower stagnations

Conclusion: Maybe cuz of the randomess throughout in case of such high-varied rewards distribution functions the algorithm fails sometimes in the MULTI-BANDIT problrm statemnt
