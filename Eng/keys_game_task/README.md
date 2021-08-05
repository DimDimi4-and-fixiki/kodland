## In this task you need add an animation of jumping, when user presses the `space` button  
We will use the same animations for `left and right` as we did at the lesson  
```python
import pygame

WIDTH = 300
HEIGHT = 250

FPS = 30
BLUE = (0,0,255)
WHITE = (255,255,255)

pygame.init()
screen = pygame.display.set_mode((WIDTH, HEIGHT))
clock = pygame.time.Clock()

x = WIDTH // 2
y = HEIGHT // 2
r = 10
screen.fill(WHITE)
pygame.draw.circle(screen, BLUE, (x, y), r)
pygame.display.update()

motion = ''
running = True
while running:
    
    events = pygame.event.get()
    for i in events:
        if i.type == pygame.QUIT:
            running = False
        if i.type == pygame.KEYDOWN:
            if i.key == pygame.K_LEFT:
                motion = 'Left'
            if i.key == pygame.K_RIGHT:
              motion = "Right"
            # JUMP CASE
            if i.key == pygame.K_SPACE:
                motion = "Up"
                 
        if i.type == pygame.KEYUP:
            if i.key == pygame.K_LEFT:
                motion = 'Stop'
            if i.key == pygame.K_RIGHT:
              motion = "Stop"
        
    # Starts moving the ball up
    if motion == "Up":
        y -= 2
        screen.fill(WHITE)
        pygame.draw.circle(screen, BLUE, (x, y), r)
    
    # If ball is high enough, it is time to move it down
    if y < 100:
        motion="Down"
    
    # Moves the ball down
    if motion == "Down":
        y += 2
        screen.fill(WHITE)
        pygame.draw.circle(screen, BLUE, (x, y), r)

        # If ball has landed, it is time to stop
        if y > 125:
            motion = "Stop"
    
    if motion == 'Left':
        x = x - 3;
        screen.fill(WHITE)
        pygame.draw.circle(screen, BLUE, (x, y), r)
    elif motion == "Right":
      x += 3
      screen.fill(WHITE)
      pygame.draw.circle(screen, BLUE, (x, y), r)
    pygame.display.update()
    clock.tick(FPS)
pygame.quit()
```
