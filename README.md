import pygame
import random

# Initialize Pygame
pygame.init()

# Screen dimensions
screen_width = 800
screen_height = 800

# Colors
white = (255, 255, 255)
black = (0, 0, 0)
red = (255, 0, 0)
green = (0, 255, 0)
blue = (0, 0, 255)
yellow = (255, 255, 0)

# Create the game window
screen = pygame.display.set_mode((screen_width, screen_height))
pygame.display.set_caption("Ludo")

# Load images (replace with your own images)
board_img = pygame.image.load("board.png")
red_token_img = pygame.image.load("red_token.png")
green_token_img = pygame.image.load("green_token.png")
blue_token_img = pygame.image.load("blue_token.png")
yellow_token_img = pygame.image.load("yellow_token.png")
dice_img = pygame.image.load("dice.png")

# Game loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Draw the board
    screen.blit(board_img, (0, 0))

    # Draw the tokens (replace with actual token positions)
    screen.blit(red_token_img, (100, 100))
    screen.blit(green_token_img, (200, 200))
    screen.blit(blue_token_img, (300, 300))
    screen.blit(yellow_token_img, (400, 400))

    # Roll the dice (replace with actual dice rolling logic)
    dice_value = random.randint(1, 6)
    screen.blit(dice_img, (500, 500))

    pygame.display.update()

pygame.quit()

