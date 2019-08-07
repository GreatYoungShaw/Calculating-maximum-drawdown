# Calculating-maximum-drawdown
In quantative finance world, maximum drawdown is an important factor in strategy choosing, even more important than sharpe ratio

To get the maximum drawdown within fastest time, the time complexity O(N) is a cosideration.

In slow algo, drawdown in done through data traversing of differential value. which is X = max(array[0:i+1)
Overall complexity being O(N^2)

In fast algo, drawdown is completed through comparsion, which is X = max(array[i+1], previous max value)
Overall complexity being O(N)

Ofcourse, python one line code with inserted function is 
np.argmax((np.maximum.accumulate(Asset) - Asset) / np.maximum.accumulate(Asset)) 

