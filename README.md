# modelo-final
from abc import ABC, abstractmethod
from datetime import datetime

class MaterialReciclado(ABC):
    def __init__(self, peso, fecha):
        self.peso = peso
        self.fecha = fecha

         @abstractmethod
    def calcular_puntos(self):
        pass

class Plastico(MaterialReciclado):
    def calcular_puntos(self):
        return self.peso * 2

class Vidrio(MaterialReciclado):
    def calcular_puntos(self):
        return self.peso * 1.5

class Lata(MaterialReciclado):
    def calcular_puntos(self):
        return self.peso * 0.5

