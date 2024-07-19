BUILD_BASE_DIR=_build
BUILD_DIR=release
BUILD_TYPE=Release

all: release			#: Build the release version
build:					#: Build the software based in BUILD_DIR and BUILD_TYPE variables
	cmake --build $(BUILD_BASE_DIR)/$(BUILD_DIR) -j $(NUM_THREADS)
release:				#: Build the release version
	$(MAKE) cmake BUILD_DIR=release BUILD_TYPE=Release && \
	$(MAKE) build BUILD_DIR=release
cmake:					#: Use CMake to create a Makefile build system
	mkdir -p $(BUILD_BASE_DIR)/$(BUILD_DIR) && \
	cmake -B \
		"$(BUILD_BASE_DIR)/$(BUILD_DIR)" \
		${CMAKE_FLAGS} \
		$(GENERATOR) \
		$(USE_CCACHE) \
		$(FORCE_COLOR) \
		${EXTRA_CMAKE_FLAGS}

