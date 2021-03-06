
set(name mobility)

set(source_files
        model/box.cc
        model/constant-acceleration-mobility-model.cc
        model/constant-position-mobility-model.cc
        model/constant-velocity-helper.cc
        model/constant-velocity-mobility-model.cc
        model/gauss-markov-mobility-model.cc
        model/geographic-positions.cc
        model/hierarchical-mobility-model.cc
        model/mobility-model.cc
        model/position-allocator.cc
        model/random-direction-2d-mobility-model.cc
        model/random-walk-2d-mobility-model.cc
        model/random-waypoint-mobility-model.cc
        model/rectangle.cc
        model/steady-state-random-waypoint-mobility-model.cc
        model/waypoint.cc
        model/waypoint-mobility-model.cc
        helper/mobility-helper.cc
        helper/ns2-mobility-helper.cc
        )

set(header_files
        model/box.h
        model/constant-acceleration-mobility-model.h
        model/constant-position-mobility-model.h
        model/constant-velocity-helper.h
        model/constant-velocity-mobility-model.h
        model/gauss-markov-mobility-model.h
        model/geographic-positions.h
        model/hierarchical-mobility-model.h
        model/mobility-model.h
        model/position-allocator.h
        model/rectangle.h
        model/random-direction-2d-mobility-model.h
        model/random-walk-2d-mobility-model.h
        model/random-waypoint-mobility-model.h
        model/steady-state-random-waypoint-mobility-model.h
        model/waypoint.h
        model/waypoint-mobility-model.h
        helper/mobility-helper.h
        helper/ns2-mobility-helper.h
        )

set(libraries_to_link ${libnetwork})

set(test_sources
        test/mobility-test-suite.cc
        test/mobility-trace-test-suite.cc
        test/ns2-mobility-helper-test-suite.cc
        test/steady-state-random-waypoint-mobility-model-test.cc
        test/waypoint-mobility-model-test.cc
        test/geo-to-cartesian-test.cc
        test/rand-cart-around-geo-test.cc
        )

build_lib("${name}" "${source_files}" "${header_files}" "${libraries_to_link}" "${test_sources}")

