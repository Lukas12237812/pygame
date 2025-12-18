import pygame
import sys

pygame.init()

# Fenster
BREITE = 900
HOEHE = 500
fenster = pygame.display.set_mode((BREITE, HOEHE))
pygame.display.set_caption("Mein Handball-Spiel")

# Farben
GRUEN = (40, 160, 60)
WEISS = (255, 255, 255)

clock = pygame.time.Clock()

# Spiel-Schleife
while True:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()

    fenster.fill(GRUEN)

    # Mittellinie
    pygame.draw.line(fenster, WEISS, (BREITE//2, 0), (BREITE//2, HOEHE), 5)

    pygame.display.update()
    clock.tick(60)


