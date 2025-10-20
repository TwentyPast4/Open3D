target_sources(tests PRIVATE
    Eigen.cpp
    FileSystem.cpp
    Helper.cpp
    IJsonConvertible.cpp
    ISAInfo.cpp
    Logging.cpp
    Preprocessor.cpp
    ProgressBar.cpp
    Timer.cpp
    Random.cpp
)

if (BUILD_DOWNLOAD_UTILITIES)
    target_sources(tests PRIVATE
            Extract.cpp # internally relies on download
            Download.cpp
    )
endif()

if (BUILD_ISPC_MODULE)
    target_sources(tests PRIVATE
        Helper.ispc
    )
endif()
