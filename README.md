# Car_dealership
import streamlit as st

st.set_page_config(layout="wide")

class car:
    def __init__(self,make,model,price,year):
      self.make = make
      self.model = model
      self.price= price
      self.year = year  

# This is just a list of car objects
inventory = [
    car("Toyota", "Hilux", 450000, 2022)
]   
# The "Web" part:
st.title("Riity's Car Dealership")
st.write("Welcome to our online showroom!")

# Using a loop to display each car on the site
for car in inventory:
    st.header(f"{car.year} {car.make} {car.model}")
    st.write(f"Price: M{car.price}")
    
    # A simple web button
    if st.button(f"Buy the {car.model}"):
        st.success(f"Great choice! You just bought the {car.model}!")
    
    st.divider()
