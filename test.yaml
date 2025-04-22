import unittest
from utils import calculer_moyenne, convertir_temperature

class TestUtils(unittest.TestCase):

    def test_calculer_moyenne(self):
        self.assertEqual(calculer_moyenne([1, 2, 3, 4, 5]), 3)
        self.assertEqual(calculer_moyenne([10, 10, 10]), 10)
        self.assertAlmostEqual(calculer_moyenne([1, 2]), 1.5)
        self.assertRaises(ZeroDivisionError, calculer_moyenne, [])

    def test_convertir_temperature_c_to_f(self):
        self.assertEqual(convertir_temperature(0, 'C', 'F'), 32)
        self.assertEqual(convertir_temperature(100, 'C', 'F'), 212)
        self.assertAlmostEqual(convertir_temperature(25, 'C', 'F'), 77)

    def test_convertir_temperature_f_to_c(self):
        self.assertEqual(convertir_temperature(32, 'F', 'C'), 0)
        self.assertEqual(convertir_temperature(212, 'F', 'C'), 100)
        self.assertAlmostEqual(convertir_temperature(77, 'F', 'C'), 25)

    def test_convertir_temperature_invalid(self):
        with self.assertRaises(ValueError):
            convertir_temperature(100, 'X', 'C')
        with self.assertRaises(ValueError):
            convertir_temperature(100, 'C', 'X')

if __name__ == '__main__':
    unittest.main()
