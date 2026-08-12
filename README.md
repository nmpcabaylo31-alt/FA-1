# FA-1

"""
Distance Calculator
--------------------
Calculates the straight-line (Euclidean) distance between two points
on a 2D plane, given their (x, y) coordinates.

Formula used:
    distance = math.sqrt (math.pow (x2 - x1,2) + math.pow (y2 - y1,2))
"""

import math


def get_point(point_label):
    """
    Ask the user to enter the x and y coordinates of a point.

    point_label: a short label used in the prompt, e.g. "first" or "second"
    Returns a tuple (x, y) of floats.
    """
    x = float(input(f"Enter the x-coordinate of the {point_label} point: "))
    y = float(input(f"Enter the y-coordinate of the {point_label} point: "))
    return x, y


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

    # Get both points from the user
    first_point = get_point("first")
    second_point = get_point("second")

    # Compute and display the result
    result = calculate_distance(first_point, second_point)
    print(f"\nThe distance between {first_point} and {second_point} "
          f"is {result:.2f} units.")


if __name__ == "__main__":
    main()
