cmake_minimum_required(VERSION 3.24)
project(ScoreboardRankViewer)

set(CMAKE_CXX_STANDARD 17)

file(GLOB_RECURSE Sources "source/*.cpp")
file(GLOB_RECURSE Headers "source/*.h")

file(GLOB_RECURSE Libraries "library/*.lib")

add_library(ScoreboardRankViewerDLL SHARED ${Sources} ${Headers})

target_include_directories(ScoreboardRankViewerDLL PRIVATE "include")
target_link_libraries(ScoreboardRankViewerDLL PRIVATE ${Libraries})
