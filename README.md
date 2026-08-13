import math

"""
Distance Calculator
--------------------
Calculates the Euclidean distance between two points.

Formula:
distance = sqrt((x2 - x1)^2 + (y2 - y1)^2)
"""

def get_coordinate(label):
    # Get a coordinate value from the user
        return float(input(f"Enter {label}: "))


        def calculate_distance(a, b):
            # Calculate distance using the Pythagorean theorem
                x1, y1 = a
                    x2, y2 = b
                        return math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2)


                        def main():
                            print("=== Distance Calculator ===")

                                # Get coordinates: x2, x1, y2, y1
                                    x2 = get_coordinate("x2")
                                        x1 = get_coordinate("x1")
                                            y2 = get_coordinate("y2")
                                                y1 = get_coordinate("y1")

                                                    point1 = (x1, y1)
                                                        point2 = (x2, y2)

                                                            # Display result
                                                                distance = calculate_distance(point1, point2)
                                                                    print(f"\nThe distance between {point1} and {point2} is {distance:.2f} units.")


                                                                    if __name__ == "__main__":
                                                                        main()
