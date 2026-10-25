# CS50P Python Practice & Week 01 Reflection

## CS50P Week 0 Practice Script

Below is a simple Python program written during CS50P Week 0 study. It calculates clock period given frequency in MHz:

```python
def calculate_period(frequency_mhz):
    if frequency_mhz <= 0:
        return "Frequency must be greater than zero."
    period_ns = 1000 / frequency_mhz
    return period_ns

def main():
    try:
        freq = float(input("Enter clock frequency in MHz: "))
        period = calculate_period(freq)
        if isinstance(period, float):
            print(f"Clock Period: {period:.2f} ns")
        else:
            print(period)
    except ValueError:
        print("Invalid input! Please enter a numerical value.")

if __name__ == "__main__":
    main() 



jjk
