############################################################################
# Copyright (c) 2018-2022 by the Cabana authors                            #
# All rights reserved.                                                     #
#                                                                          #
# This file is part of the Cabana library. Cabana is distributed under a   #
# BSD 3-clause license. For the licensing terms see the LICENSE file in    #
# the top-level directory.                                                 #
#                                                                          #
# SPDX-License-Identifier: BSD-3-Clause                                    #
############################################################################

  add_executable(HaloExchange halo_exchange_example.cpp)
  target_link_libraries(HaloExchange cabanacore)
  add_test(NAME Core_tutorial_12 COMMAND ${MPIEXEC} ${MPIEXEC_NUMPROC_FLAG}
    ${MPIEXEC_MAX_NUMPROCS} ${MPIEXEC_PREFLAGS} ${CMAKE_CURRENT_BINARY_DIR}/HaloExchange ${MPIEXEC_POSTFLAGS})
  set_tests_properties(Core_tutorial_12 PROPERTIES PROCESSORS ${MPIEXEC_MAX_NUMPROCS})
