1. Continuous data refers to an amount, that is, data where the values could be any amount within a range, such as the amount of money in each bank account at a bank. Ordinal data is data that determines the order of something, like indexing in Python. The value of an index can tell you where to find a piece of data in a string, list or data frame, but you wouldn't learn anything by adding or subtracting ordinal data. Finally, nominal data is used to display non-numerical data as numbers. For example, the Gapminder data lists countries and the continents they're on. However, if we wanted to save space, we could instead fill this column with numbers, with each representing a specific continent on a key, rather than spelling the names of continents out every time.

2. I was confused by this question and will ask about it on Friday.

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