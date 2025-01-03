build kernel a33 tutorial=


export PATH=$(pwd)/pronton-toolchains-a33/clang/host/linux-x86/clang-r416183b/bin:$PATH
export PATH=$(pwd)/pronton-toolchains-a33/build/build-tools/path/linux-x86:$(pwd)/pronton-toolchains-a33/prebuilts/gas/linux-x86:$PATH

make PLATFORM_VERSION=14 ANDROID_MAJOR_VERSION=u LLVM=1 LLVM_IAS=1 ARCH=arm64 TARGET_SOC=s5e8825 CROSS_COMPILE=$(pwd)/pronton-toolchains-a33/clang/host/linux-x86/clang-r416183b/bin/aarch64-linux-gnu- s5e8825-a33xub_defconfig
make PLATFORM_VERSION=14 ANDROID_MAJOR_VERSION=s LLVM=1 LLVM_IAS=1 ARCH=arm64 TARGET_SOC=s5e8825 CROSS_COMPILE=$(pwd)/pronton-toolchains-a33/clang/host/linux-x86/clang-r416183b/bin/aarch64-linux-gnu- -j32
