find_package(SDL2 REQUIRED)
add_library(sdl_gfx)

target_sources(sdl_gfx PRIVATE
        SDL2_framerate.c
        SDL2_gfxPrimitives.c
        SDL2_imageFilter.c
        SDL2_rotozoom.c
)

target_link_libraries(sdl_gfx PUBLIC
        SDL2::SDL2
)
target_link_directories(sdl_gfx PUBLIC
        ${SDL2_INCLUDE_DIRS}
)