# Triangle567
import unittest
from classify_triangle import classifyTriangle

class TestClassifyTriangle(unittest.TestCase):
    def test_equilateral_triangle(self):
        self.assertEqual(classifyTriangle(3, 3, 3), "Equilateral")

    def test_isosceles_triangle(self):
        self.assertEqual(classifyTriangle(3, 4, 3), "Isoceles")

    def test_scalene_triangle(self):
        self.assertEqual(classifyTriangle(3, 4, 5), "Scalene")

    def test_not_a_triangle(self):
        self.assertEqual(classifyTriangle(1, 1, 2), "NotATriangle")

    def test_right_angled_triangle(self):
        self.assertEqual(classifyTriangle(3, 4, 5), "Right")

    def test_invalid_input(self):
        self.assertEqual(classifyTriangle(201, 3, 4), "InvalidInput")

if __name__ == "__main__":
    unittest.main()

