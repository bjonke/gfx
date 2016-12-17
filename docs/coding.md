    SDL and SDL2 Clearing a screen in a certain color
    
    //Initialization
    SDL_Init(SDL_INIT_EVERYTHING);

    //Window
    SDL_Window *MainWindow = SDL_CreateWindow("My Game Window",
                                  SDL_WINDOWPOS_CENTERED,
                                  SDL_WINDOWPOS_CENTERED,
                                  640, 480,
                                  SDL_WINDOW_SHOWN
                                  );

    //Renderer
    SDL_Renderer *Background = SDL_CreateRenderer(MainWindow, -1, 0);

    SDL_SetRenderDrawColor(Background, 255, 255, 255, 255);

    SDL_RenderClear(Background);

    SDL_Delay(3000);

    //Clean up
    SDL_DestroyWindow(MainWindow);
    SDL_Quit();
