# prograpia
PROGRAMACION AVANZADA
"a) Genere una clase en Python llamada TDevice (Dispositivo Electrónico)"
class TDevice:
    def __init__(self, tamaño, peso, altura, marca):
        self.tamaño = tamaño
        self.peso = peso
        self.altura = altura
        self.marca = marca
        self.encendido = False

    def encender(self):
        self.encendido = True
        print("El dispositivo ha sido encendido.")

    def apagar(self):
        self.encendido = False
        print("El dispositivo ha sido apagado.")
        
        
        
        
        
        
        
        "b) Genere 3 clases que desciendan de TDevice "
class TV(TDevice):
    def cambiar_canal(self, canal):
        print(f"Cambiando al canal {canal}.")

    def ajustar_volumen(self, volumen):
        print(f"Ajustando volumen a {volumen}.")

    def reproducir(self):
        print("Reproduciendo contenido.")

class Licuadora(TDevice):
    def triturar(self, velocidad):
        print(f"Triturando a velocidad {velocidad}.")

    def mezclar(self, tiempo):
        print(f"Mezclando durante {tiempo} segundos.")

    def pausa(self):
        print("Pausando la licuadora.")

class Celular(TDevice):
    def llamar(self, numero):
        print(f"Llamando al número {numero}.")

    def enviar_mensaje(self, mensaje):
        print(f"Enviando mensaje: {mensaje}.")

    def tomar_foto(self):
        print("Tomando una foto.")
        




"c) Genere 2 instancias de cada una de las clases"
tv1 = TV("Grande", "2kg", "60cm", "Samsung")
tv2 = TV("Pequeña", "1kg", "40cm", "LG")

licuadora1 = Licuadora("Grande", "3kg", "40cm", "Oster")
licuadora2 = Licuadora("Pequeña", "2kg", "30cm", "Hamilton Beach")

celular1 = Celular("Pequeño", "0.2kg", "15cm", "iPhone")
celular2 = Celular("Mediano", "0.3kg", "16cm", "Samsung")




"d) Genere una clase llamada TPersona con 5 atributos y 5 funciones."
class TPersona:
    def __init__(self, nombre, edad, genero, altura, peso):
        self.nombre = nombre
        self.edad = edad
        self.genero = genero
        self.altura = altura
        self.peso = peso

    def hablar(self):
        print("La persona está hablando.")

    def caminar(self):
        print("La persona está caminando.")

    def comer(self):
        print("La persona está comiendo.")

    def dormir(self):
        print("La persona está durmiendo.")

    def trabajar(self):
        print("La persona está trabajando.")






"e) Genere 3 clases que desciendan de TPersona"
class Policia(TPersona):
    def arrestar(self):
        print("El policía está arrestando.")

    def patrullar(self):
        print("El policía está patrullando.")

    def interrogar(self):
        print("El policía está interrogando.")

class Administrador(TPersona):
    def organizar(self):
        print("El administrador está organizando.")

    def supervisar(self):
        print("El administrador está supervisando.")

    def coordinar(self):
        print("El administrador está coordinando.")

class Bombero(TPersona):
    def apagar_incendio(self):
        print("El bombero está apagando un incendio.")

    def rescatar(self):
        print("El bombero está realizando un rescate.")

    def entrenar(self):
        print("El bombero está entrenando.")





"f) Genere 1 clase que descienda "
class TArea(TPolicia, TAdministrador, TBombero):
    def __init__(self, nombre, edad, genero, altura, peso, area):
        super().__init__(nombre, edad, genero, altura, peso)
        self.area = area

    def gestionar(self):
        print(f"El empleado de {self.area} está gestionando.")





"g) Instanciar 2 veces cada una de las clases"
policia1 = Policia("Juan", 35, "Masculino", "1.80m", "80kg")
policia2 = Policia("María", 40, "Femenino", "1.65m", "70kg")

administrador1 = Administrador("Pedro", 45, "Masculino", "1.75m", "75kg")
administrador2 = Administrador("Laura", 38, "Femenino", "1.70m", "65kg")

bombero1 = Bombero("Carlos", 30, "Masculino", "1.85m", "85kg")
bombero2 = Bombero("Ana", 32, "Femenino", "1.60m", "60kg")





"h) Define una clase llamada Persona que tenga los siguientes atributos: nombre, edad"
class Persona:
    def __init__(self, nombre, edad, genero):
        self.nombre = nombre
        self.edad = edad
        self.genero = genero

    def presentarse(self):
        print(f"Hola, me llamo {self.nombre} y tengo {self.edad} años.")




"i) Crea una subclase llamada Estudiante que herede de la clase Persona y tenga un"
"atributo adicional llamado curso"
class Estudiante(Persona):
    def __init__(self, nombre, edad, genero, curso):
        super().__init__(nombre, edad, genero)
        self.curso = curso

    def estudiar(self):
        print(f"Estoy estudiando el curso de {self.curso}.")




"j) Define una clase llamada Rectángulo que tenga dos atributos: largo y ancho. "
class Rectangulo:
    def __init__(self, largo, ancho):
        self.largo = largo
        self.ancho = ancho

    def area(self):
        return self.largo * self.ancho

