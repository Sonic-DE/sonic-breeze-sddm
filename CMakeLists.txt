cmake_minimum_required(VERSION 3.16)

project(sonic-breeze-sddm VERSION 6.8.0 LANGUAGES CXX)

set(KF6_MIN_VERSION "6.26.0")

find_package(ECM ${KF6_MIN_VERSION} REQUIRED NO_MODULE)
set(CMAKE_MODULE_PATH ${ECM_MODULE_PATH})

include(KDEInstallDirs)
include(FeatureSummary)

add_subdirectory(breeze-sddm-theme)

feature_summary(WHAT ALL FATAL_ON_MISSING_REQUIRED_PACKAGES)
