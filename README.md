# bolo-de-aniversario
o código cria três bolos de aniversário.  

import turtle
tela=turtle.Screen()
input("precione ENTER para continuar")
def desenha_bolinho_da_manu(*args):
    for arg in args:
        x, y, zoom = arg
        turtle.up()
        turtle.goto(x, y - 150 * zoom)
        turtle.begin_fill()
        turtle.fillcolor("brown")
        turtle.down()
        turtle.goto(x, y - 75 * zoom)
        turtle.goto(x + 170 * zoom, y - 75 * zoom)
        turtle.goto(x + 170 * zoom, y - 150 * zoom)
        turtle.goto(x, y - 150 * zoom)
        turtle.end_fill()

        turtle.up()
        turtle.goto(x, y - 75 * zoom)
        turtle.begin_fill()
        turtle.fillcolor("pink")
        turtle.down()
        turtle.goto(x + 170 * zoom, y - 75 * zoom)
        turtle.goto(x + 170 * zoom, y - 60 * zoom)
        turtle.goto(x, y - 60 * zoom)
        turtle.goto(x, y - 75 * zoom)
        turtle.end_fill()

        turtle.up()
        turtle.goto(x, y + 15 * zoom)
        turtle.begin_fill()
        turtle.fillcolor("brown")
        turtle.down()
        turtle.goto(x, y - 60 * zoom)
        turtle.goto(x + 170 * zoom, y - 60 * zoom)
        turtle.goto(x + 170 * zoom, y + 15 * zoom)
        turtle.goto(x, y + 15 * zoom)
        turtle.end_fill()

        for i in range(0, 150, 25):
            turtle.up()
            turtle.goto(x + (25 + i) * zoom, y + 15 * zoom)
            turtle.begin_fill()
            turtle.fillcolor("yellow")
            turtle.down()
            turtle.goto(x + (25 + i) * zoom, y + 45 * zoom)
            turtle.goto(x + (30 + i) * zoom, y + 45 * zoom)
            turtle.goto(x + (30 + i) * zoom, y + 15 * zoom)
            turtle.end_fill()       
# Chamando a função para desenhar vários bolos em posições diferentes 
desenha_bolinho_da_manu((0, 0, 1), (200, -200, 0.5), (-200, 200, 1),)


turtle.done()
