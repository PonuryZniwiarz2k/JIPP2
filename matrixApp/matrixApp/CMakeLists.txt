cmake_minimum_required(VERSION 3.16)

set(CMAKE_CXX_STANDARD  17)

# Dodajemy ścieżkę, w której mają być wyszukiwane pliki nagłówkowe
include_directories(../matrixLib/include)

# Dodajemy pliki do kompilacji
add_executable(matrixApp main.cpp)

# Załączamy do naszej aplikacji biblioteki. Musi to być po add_executable
target_link_libraries(matrixApp PUBLIC matrixLib)