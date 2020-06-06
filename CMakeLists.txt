cmake_minimum_required(VERSION 3.16)
project(tf2_bot_detector)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wall -Werror")

# GCC-10
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Werror")
add_compile_options(-fcoroutines)


# Clang
#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -std=c++2a -stdlib=libstdc++")



include_directories(submodules/nlohmann_json/include)
include_directories(submodules/mh_stuff/cpp/include)
include_directories(submodules/implot)
include_directories(submodules/imgui_desktop/imgui_desktop/include)
include_directories(tf2_bot_detector)
include_directories(tf2_bot_detector/Config)
include_directories(tf2_bot_detector/PlatformSpecific)

add_executable(tf2_bot_detector
        tf2_bot_detector/Config/JSONHelpers.h
        tf2_bot_detector/Config/PlayerListJSON.cpp
        tf2_bot_detector/Config/PlayerListJSON.h
        tf2_bot_detector/Config/Rules.cpp
        tf2_bot_detector/Config/Rules.h
        tf2_bot_detector/Config/Settings.cpp
        tf2_bot_detector/Config/Settings.h
        tf2_bot_detector/PlatformSpecific/Windows/CrashHandler.cpp
        tf2_bot_detector/PlatformSpecific/Windows/Shell.cpp
        tf2_bot_detector/PlatformSpecific/Shell.h
        tf2_bot_detector/ActionManager.cpp
        tf2_bot_detector/ActionManager.h
        tf2_bot_detector/Actions.cpp
        tf2_bot_detector/Actions.h
        tf2_bot_detector/Clock.cpp
        tf2_bot_detector/Clock.h
        tf2_bot_detector/CompensatedTS.cpp
        tf2_bot_detector/CompensatedTS.h
        tf2_bot_detector/ConsoleLines.cpp
        tf2_bot_detector/ConsoleLines.h
        tf2_bot_detector/ICommandSource.h
        tf2_bot_detector/IConsoleLine.h
        tf2_bot_detector/IConsoleLineListener.h
        tf2_bot_detector/ImGui_TF2BotDetector.cpp
        tf2_bot_detector/ImGui_TF2BotDetector.h
        tf2_bot_detector/IPlayer.cpp
        tf2_bot_detector/IPlayer.h
        tf2_bot_detector/IWorldEventListener.h
        tf2_bot_detector/LobbyMember.h
        tf2_bot_detector/Log.cpp
        tf2_bot_detector/Log.h
        tf2_bot_detector/main.cpp
        tf2_bot_detector/MainWindow.cpp
        tf2_bot_detector/MainWindow.h
        tf2_bot_detector/ModeratorLogic.cpp
        tf2_bot_detector/ModeratorLogic.h
        tf2_bot_detector/NetworkStatus.cpp
        tf2_bot_detector/NetworkStatus.h
        tf2_bot_detector/PathUtils.cpp
        tf2_bot_detector/PathUtils.h
        tf2_bot_detector/PeriodicActions.cpp
        tf2_bot_detector/PeriodicActions.h
        tf2_bot_detector/PlayerStatus.h
        tf2_bot_detector/RegexHelpers.h
        tf2_bot_detector/SetupFlow.cpp
        tf2_bot_detector/SetupFlow.h
        tf2_bot_detector/SteamID.cpp
        tf2_bot_detector/SteamID.h
        tf2_bot_detector/TFConstants.h
        tf2_bot_detector/WorldState.cpp
        tf2_bot_detector/WorldState.h)
