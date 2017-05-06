set(DIRS
    ar
    kind
    sdf
    pcp
    usd
    usdUtils
)

foreach(d ${DIRS})
    add_subdirectory(${d})
endforeach()

