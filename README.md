# Reto4


class Series():


    # propiedades
    Titulo = ''
    Numero_de_temporadas = '3'
    Entregado = 'false'
    Genero = ''
    Creador = ''

    # constructor

    def __init__(self, Titulo, Numero_de_temporadas, Entregado, Genero, Creador):
        self.Titulo = Titulo
        self.Numero_de_temporadas = Numero_de_temporadas
        self.Entregado = False
        self.Genero = Genero
        self.Creador = Creador

    # Get  / set

    def get_Titulo(self):
        return self.Titulo

    def set_Titulo(self, Titulo):
        self.__Titulo = Titulo

    def get_Numero_de_temporadas(self):
        return self.Numero_de_temporadas

    def set_Numero_de_temporadas(self, Numero_de_temporadas):
        self.__Numero_de_temporadas = Numero_de_temporadas

    def get_Genero(self):
        return self.__Genero

    def set_Genero(self, Genero):
        self.__Genero = Genero

    def get_Creador(self):
        return self.__Creador

    def set_Creador(self, Creador):
        self.__Creador = Creador



    
    def __str__(self):
        texto = "Titulo: {0}, Numero_de_temporadas {1}, Entregado {2}, Genero {3}, Creador {4} "
        return texto.format(self.Titulo, self.Numero_de_temporadas, self.Entregado, self.Genero, self.Creador)




class Video_Juegos():


    # propiedades
    Titulo_del_videojuego = ''
    Horas_estimadas = '10'
    Entregado = 'false'
    Genero = ''
    Compania = ''

    # constructor

    def __init__(self, Titulo_del_videojuego, Horas_estimadas, Entregado, Genero, Compania):
          self.Titulo_del_videojuego = Titulo_del_videojuego
          self.Horas_estimadas = Horas_estimadas
          self.Entregado = False
          self.Genero = Genero
          self.Compania = Compania

    # Get / set

    def get_Titulo_del_videojuego(self):
     return self.Titulo_del_videojuego

    def set_Titulo_del_videojuego(self, Titulo_del_videojuego):
        self.__Titulo_del_videojuego = Titulo_del_videojuego

    def get_Horas_estimadas(self):
        return self.__Horas_estimadas

    def set_Horas_estimadas(self, Horas_estimadas):
        self.__Horas_estimadas = Horas_estimadas

    def get_Genero(self):
        return self.__Genero

    def set_Genero(self, Genero):
        self.__Genero = Genero

    def get_Compania(self):
        return self.__Compania

    def set_Compania(self, Compania):
        self.__Compania = Compania


    def __str__(self):
        texto = "Titulo_del_videojuego: {0}, Horas_estimadas: {1}, Entregado: {2}, Genero: {3}, Compania: {4} "
        return texto.format(self.Titulo_del_videojuego, self.Horas_estimadas, self.Entregado, self.Genero, self.Compania)


class Entregable():

    def entregar(self):

        self.entregar = True

    def devolver(self):

        self.devolver = False

    for e in  Series:
        if Series.isEntregado(e) == True:
            print("la serie" + e.Titulo + "estaba entregado, y ahora se ha devuelto")
            Series.devolver(e)

    for e in Video_Juegos:
        if Video_Juegos.isEntregado(e) == True:
            print("el video juego" + e.Titulo_del_videojuego + "estaba entregado, y ahora se ha devuelto")
            Video_Juegos.devolver(e)



    class lista_de_serie():
        series = []

        def mostrar_lista_de_series(self):
            for Serie in self.series:
                print(Serie.Titulo)

        def add_serie(self, Serie):
            self.series.append(Serie)

        S1 = Series('stranger things', 'terror', 'Matt y Ross Duffer')
        S2 = Series('Dark', 'Misterio', ' Baran bo Odar')
        S3 = Series('Pálpito', 'drama', ' Leonardo Padrón')
        S4 = Series('Control Z', 'Drama', 'Carlos Quintanilla Sakar')
        S5 = Series('Black Mirror', 'Ciencia ficción', 'Charlie Brooker')

        Series = Series()

        series.add_serie(S1)
        series.add_serie(S2)
        series.add_serie(S3)
        series.add_serie(S4)
        series.add_serie(S5)

        series.mostrar_series()


    class lista_de_Video_juegos():
       Video_juegos = []

    def mostrar_lista_de_Video_juegos(self):
        for Serie in self.Video_juegos:
            print(Video_Juegos.Titulo)

    def add_serie(self, Serie):
        self.series.append(Serie)

      S1 = Series('stranger things', 'terror', 'Matt y Ross Duffer')
      S2 = Series('Dark', 'Misterio', ' Baran bo Odar')
      S3 = Series('Pálpito', 'drama', ' Leonardo Padrón')
      S4 = Series('Control Z', 'Drama', 'Carlos Quintanilla Sakar')
      S5 = Series('Black Mirror', 'Ciencia ficción', 'Charlie Brooker')

      Series = Series()

      Video_Juegos.add_Video_juegos(S1)
      Video_Juegos.add_Video_juegos(S2)
      Video_Juegos.add_Video_juegos(S3)
      Video_Juegos.add_Video_juegos(S4)
      Video_Juegos.add_Video_juegos(S5)

      Video_Juegos.mostrar_Video_juegos()

    def __str__(self):
            texto = "Titulo_del_videojuego: {0}, Horas_estimadas: {1}, Entregado: {2}, Genero: {3}, Compania: {4} "
            return texto.format(self.Titulo_del_videojuego, self.Horas_estimadas, self.Entregado, self.Genero,self.Compania)

            print('El Videojuego tiene más horas estimadas es:')
            print(Video_Juegos[0])  # El videojuego con más horas estimadas


    def __str__(self):
        texto = "Titulo: {0}, Numero_de_temporadas {1}, Entregado {2}, Genero {3}, Creador {4} "
        return texto.format(self.Titulo, self.Numero_de_temporadas, self.Entregado, self.Genero, self.Creador)

            print('la serie con mayor numero de temporadas es:')
            print(Series[0])  # La serie con mayor número de temporadas
