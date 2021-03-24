1. Continuous data refers to an amount, that is, data where the values could be any amount within a range, such as the amount of money in each bank account at a bank. Ordinal data is data that determines the order of something, like indexing in Python. The value of an index can tell you where to find a piece of data in a string, list or data frame, but you wouldn't learn anything by adding or subtracting ordinal data. Finally, nominal data is used to display non-numerical data as numbers. For example, the Gapminder data lists countries and the continents they're on. However, if we wanted to save space, we could instead fill this column with numbers, with each representing a specific continent on a key, rather than spelling the names of continents out every time.

My model might be used in the context of political science. For example, I might want to study how education level across the states affects party performance in those states. If that's the case, education level (say, percent of the population with a college degree or higher) will be the independent variable and party performance (for example, change in Democratic vote share between 2 Presidential elections) will be the target, or dependent variable.

2. 

import matplotlib.pyplot as plt
n = 1000
#np.random.seed(146)
a = 5
b = 5
x2 = np.random.beta(a, b, size=n)
np.mean(x2)
np.median(x2)

#setting a and b equal to something, a decimal in one case and a decimal >1 but <2 in another

plt.figure(figsize=(8, 8))
plt.hist(x2)
plt.show()

![image](https://user-images.githubusercontent.com/78311527/112394254-c4572b80-8cd2-11eb-9423-94bbe8411f41.png)

This data has a mean that approximates the 50th percentile (minimal skew), with a mean of 0.5057072038373106 and a median of 0.5065650801448449.

n = 1000
#np.random.seed(146)
a = 0.57
b = 1.32
x2 = np.random.beta(a, b, size=n)
np.mean(x2)
np.median(x2)

#setting a and b equal to something, a decimal in one case and a decimal >1 but <2 in another

plt.figure(figsize=(8, 8))
plt.hist(x2)
plt.show()

![image](https://user-images.githubusercontent.com/78311527/112394312-e18bfa00-8cd2-11eb-9485-c04495cd83a8.png)

This data is skewed right with a mean of 0.2886643347664441 and a median of 0.21231592212207134.

n = 1000
#np.random.seed(146)
a = 50
b = 5
x2 = np.random.beta(a, b, size=n)
np.mean(x2)
np.median(x2)

#setting a and b equal to something, a decimal in one case and a decimal >1 but <2 in another

plt.figure(figsize=(8, 8))
plt.hist(x2)
plt.show()

![image](https://user-images.githubusercontent.com/78311527/112394131-91149c80-8cd2-11eb-9b23-c8a5822caaf3.png)

This data is skewed left with a mean of 0.9086642978791913 and median of 0.9141409200671622.

3.

import matplotlib as plt

idx_1952 = data['year']==1952
data_1952 = data[idx_1952]
idx_2007 = data['year']==2007
data_2007 = data[idx_2007]

def count_elements(a)
    hist = {}
    for i in a:
    hist[i] = hist.get(i, 0) + 1
    return hist

b = count_elements(data_1952)
c = count_elements(data_2007)

plt.hist(b, c)
plt.xlabel('Life Expectancy')
plt.ylabel('Frequency')
plt.title('Gapminder Histogram for 1952 and 2007')

plt.hist(b, c, np.log10())
plt.xlabel('Life Expectancy')
plt.ylabel('Frequency')
plt.title('Gapminder Histogram with Logarithmic Axis')

The linear model is better because the range of data isn't that big, which makes the logarithmic model unnessecary.

4.

import seaborn as sns

sns.boxplot(x=data['year'], y=data['Life Expectancy'], data=data)
sns.title('Life Expectancy by Country, 1952-2007')

sns.boxplot(x=data['year'], y=data['Life Expectancy'], data=data, np.log10())
sns.title('Life Expectancy Boxplot with Logarithmic Axis')

As was the case with question 3, the linear model is better because the range of data isn't that big. In fact, the list of years intentionally increases by 5 every time.
