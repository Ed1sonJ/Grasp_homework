CXX=E:\MinGW\bin\g++.exe
CFLAGS=
LDFLAGS=
PWD=$(shell pwd)

#size of cache in MB
CSIZE=1

# Supported values: grasp, lru, pin
POLICY=grasp
# POLICY=lru
# POLICY=pin

# Path to a directory where the trace files are located
GDIR=${DBG_ROOT}/datasets

# Name of a trace file
TRACE=BC.web-Google.cvgr.dbg.lru.llc.trace
# TRACE=BellmanFordOpt.web-Google.cintgr.dbg.lru.llc.trace
# TRACE=PageRankOpt.web-Google.cvgr.dbg.lru.llc.trace
# TRACE=PageRankDeltaOpt.web-Google.cvgr.dbg.lru.llc.trace


CFLAGS=-std=c++11

run: ${POLICY}.bin
	${PWD}/${POLICY}.bin ${GDIR}/${TRACE} ${CSIZE}

${POLICY}.bin: ${POLICY}.cpp common.h cache.h
	${CXX} ${CFLAGS} ${LDFLAGS} -o ${POLICY}.bin ${POLICY}.cpp 

clean:
	rm -rf *.bin

help:
	@echo TRACE=${TRACE};\
		echo POLICY=grasp;\
		echo CSIZE=1;\
		echo GDIR=${MEMPHIS_DATASETS};\
