![MIT Deep Traffic](https://selfdrivingcars.mit.edu/deeptraffic/car-red.png)

# MIT-Deep-Traffic-Solution
My Solution to the MIT Deep Traffic Project for MIT 6.S094. https://selfdrivingcars.mit.edu/deeptraffic/

This currently gets an average 65.725 mph with local evaluation after 20000 iterations which is just enough to get a passing grade for the project. With more iterations, it gets a higher performance. Final evaluation is 66.69. Given that I didn't invest more than 2 hours on this, I consider that to be adequate. This configuration learns slowly, but seems to consistently stay outside of a local maximum.

Some things to try if I have more time:
* Increased batch size.
* More hidden layers in the network.
* More neurons in each layer.
* More training iterations.
* Follow the graphs and insights in section 3 of this paper to further optimize learning. https://arxiv.org/pdf/1801.02805.pdf
* More intelligent cars on the road.


Note: It is advised to use either a sigmoid or tanh activation function in the last hidden layer to get zero centered results. Although you get vanishing gradients, it is important that the end result be zero centered to avoid divergence before regression at the end. Using relu in one of the hidden layers can cause growth to increase more quickly because it encourages acceleration, but can cause the car to stay in a local maximum. If you need to get a less optimal model faster, you can use relu, but if you have all the time in the world, sigmoid/tanh is recommended.
