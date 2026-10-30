import pygame

pygame.init()

WIDTH = 640
HEIGHT = 480
SIZE = (WIDTH, HEIGHT)

screen = pygame.display.set_mode(SIZE)
clock = pygame.time.Clock()

# ---------------------------
# Initialize global variables

blue = (50, 119, 168)
darkblue = (40, 91, 128)

colour1 = True
flashinterval = 500
last_switch_time = 0
current_colour = blue

# ---------------------------

running = True
while running:
    # EVENT HANDLING
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
        elif event.type == pygame.MOUSEBUTTONDOWN:
            print(event.pos)

    # GAME STATE UPDATES
    # All game math and comparisons happen here

    current_time = pygame.time.get_ticks()

    if current_time - last_switch_time > flashinterval:
        colour1 = not colour1
        last_switch_time = current_time

       
        if colour1:
            current_colour = blue
        else:
            current_colour = darkblue

    # DRAWING
  
    screen.fill((current_colour))  # always the first drawing command
    dark = (10, 10, 10)
  
    #sun:

    sun_colour = (227, 216, 64)
    sun_x = 105
    sun_y = 93

    pygame.draw.circle(screen, sun_colour, (sun_x, sun_y), 60)

    #ground:

    ground_position = (313, 843)

    pygame.draw.circle(screen, dark, (ground_position), 500)

    #trees:

    points = (438, 296), (473, 148), (507, 301)
    
    pygame.draw.polygon(screen, dark, points)

    pygame.draw.rect(screen, dark, (460, 280, 23, 98))

    points = (330, 285), (396, 291), (380, 144)
    
    pygame.draw.polygon(screen, dark, points)

    pygame.draw.rect(screen, dark, (353, 283, 23, 98))

    points = (544, 325), (600, 341), (583, 184)
    
    pygame.draw.polygon(screen, dark, points)

    pygame.draw.rect(screen, dark, (559, 328, 23, 98))

    #stars:

    stars = [(200, 100),
             (300, 300),
             (430, 63),
             (213, 234),
             (538, 155),
             (589, 50),
             (69, 299),
             (315, 161),
             (417, 237),
             (611, 379),
             (625, 222),
             (311, 36),
             (28, 196),
             (132, 211),
             (141, 342)]

    for pos in stars:
        pygame.draw.circle(screen, (255, 255, 255), pos, 5)

    # Must be the last two lines
    # of the game loop
    pygame.display.flip()
    clock.tick(30)
    #---------------------------


pygame.quit()
