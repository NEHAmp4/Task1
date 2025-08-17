# average_temperature.py

def calculate_average_temperature(temperatures):
    """
    Calculates the average temperature from a list of temperatures.

    Parameters:
    temperatures (list of float): A list of temperature readings.

    Returns:
    float: The average temperature.
    """
    if not temperatures:
        raise ValueError("Temperature list is empty.")
    
    total = sum(temperatures)
    count = len(temperatures)
    average = total / count

    return average

if __name__ == "__main__":
    # Example temperature readings (in Celsius)
    temperature_readings = [22.5, 23.0, 21.8, 24.1, 22.9]

    try:
        avg_temp = calculate_average_temperature(temperature_readings)
        print(f"Average Temperature: {avg_temp:.2f}°C")
    except ValueError as e:
        print(f"Error: {e}")

