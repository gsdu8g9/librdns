SET(REGRESSSRC dns_regress.c)

ADD_EXECUTABLE(dns_regress EXCLUDE_FROM_ALL ${REGRESSSRC})
SET_TARGET_PROPERTIES(dns_regress PROPERTIES LINKER_LANGUAGE C)

TARGET_LINK_LIBRARIES(dns_regress event)
TARGET_LINK_LIBRARIES(dns_regress ev)
TARGET_LINK_LIBRARIES(dns_regress rdns)

SET(CURVESRC dns_curve.c)

ADD_EXECUTABLE(dns_curve EXCLUDE_FROM_ALL ${CURVESRC})
SET_TARGET_PROPERTIES(dns_curve PROPERTIES LINKER_LANGUAGE C)

TARGET_LINK_LIBRARIES(dns_curve sodium)
TARGET_LINK_LIBRARIES(dns_curve ev)
TARGET_LINK_LIBRARIES(dns_curve rdns)