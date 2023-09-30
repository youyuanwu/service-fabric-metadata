add_subdirectory(fabric)
add_subdirectory(fabric_internal)

# add fabric import libs
set(FABRIC_LIB_NAMES
    FabricRuntime
    FabricClient
    FabricResources
    FabricServiceCommunication
    FabricTransport
)

foreach(_fabric_lib_name ${FABRIC_LIB_NAMES})
    add_fabric_lib(NAME ${_fabric_lib_name})
endforeach()

