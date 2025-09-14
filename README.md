# Pandas1

1 Problem 1 : Make a Pandas DataFrame with two-dimensional list	(	https://www.geeksforgeeks.org/make-a-pandas-dataframe-with-two-dimensional-list-python/)
import pandas as pd

# Two-dimensional list
data = [['Geek1', 'Reacher', 25],
        ['Geek2', 'Pete', 30],
        ['Geek3', 'Wilson', 26],
        ['Geek4', 'Williams', 22]]

# Column names
columns = ['FName', 'LName', 'Age']

# Creating DataFrame with specified data types
df = pd.DataFrame(data, columns=columns)

# Displaying the DataFrame
print(df)

2 Problem 2 :Big Countries	(	https://leetcode.com/problems/big-countries/ )
import pandas as pd

def big_countries(world: pd.DataFrame) -> pd.DataFrame:
    return world[(world["area"] >= 3000000) | (world["population"] >= 25000000)][["name","population","area"]]
    # return df[["name","population","area"]]

3 Problem 3 :Recyclable and Low Fat Products	(	https://leetcode.com/problems/recyclable-and-low-fat-products/ )
import pandas as pd

def find_products(products: pd.DataFrame) -> pd.DataFrame:
    return products[(products["low_fats"] == "Y") & (products["recyclable"]== "Y")][["product_id"]]

4 Problem 4 :Customer Who Never Order	(	https://leetcode.com/problems/customers-who-never-order/  )
import pandas as pd

def find_customers(customers: pd.DataFrame, orders: pd.DataFrame) -> pd.DataFrame:
    df = customers[~customers["id"].isin(orders["customerId"])]
    return df[["name"]].rename(columns = {"name" : "Customers"})

