#FA_1

import math


"""
Distance Calculator
--------------------
Calculates the straight-line (Euclidean) distance between two points
on a 2D plane, given their (x, y) coordinates.

Formula used:
    distance = sqrt( (x2 - x1)^2 + (y2 - y1)^2 )
"""

def get_coordinate(label):
    """
    Ask the user to enter a single coordinate value.

        label: text shown in the prompt, e.g. "x2"
            Returns the coordinate as a float.
    """
    return float(input(f"Enter {label}: "))


def calculate_distance(point_a, point_b):
    """
    Calculate the Euclidean distance between two points.

        point_a, point_b: tuples in the form (x, y)
            Returns the distance as a float.
    """
    x1, y1 = point_a
    x2, y2 = point_b

    horizontal_difference = x2 - x1
    vertical_difference = y2 - y1

    # Pythagorean theorem: c = sqrt(a^2 + b^2)
    distance = math.sqrt(horizontal_difference ** 2 + vertical_difference ** 2)
    return distance


def main():
    print("=== Distance Calculator ===")

    # Get coordinates in the order: x2, x1, y2, y1
    x2 = get_coordinate("x2")
    x1 = get_coordinate("x1")
    y2 = get_coordinate("y2")
    y1 = get_coordinate("y1")

    first_point = (x1, y1)
    second_point = (x2, y2)

    # Compute and display the result
    result = calculate_distance(first_point, second_point)
    print(f"\nThe distance between {first_point} and {second_point} "
          f"is {result:.2f} units.")


if __name__ == "__main__":
    main()
