cmake_minimum_required(VERSION 3.5)
project(rcl_interfaces)

find_package(catkin REQUIRED COMPONENTS
  message_generation
)

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  FloatingPointRange.msg
  IntegerRange.msg
  ListParametersResult.msg
  Log.msg
  ParameterDescriptor.msg
  ParameterEventDescriptors.msg
  ParameterEvent.msg
  Parameter.msg
  ParameterType.msg
  ParameterValue.msg
  SetParametersResult.msg
)

## Generate services in the 'srv' folder
add_service_files(
  FILES
  DescribeParameters.srv
  GetParameters.srv
  GetParameterTypes.srv
  ListParameters.srv
  SetParametersAtomically.srv
  SetParameters.srv
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  # DEPENDENCIES
)

###################################
## catkin specific configuration ##
###################################
catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES rcl_interfaces
  CATKIN_DEPENDS message_runtime
#  DEPENDS system_lib
)

###########
## Build ##
###########

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
