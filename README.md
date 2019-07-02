# Compares .config files, list changes except kconfig's defaults.

Usage: diffdefconfig [-d DEFCONFIG] [SOURCE] TARGET

Current directory must be in root of kernel.

If no SOURCE specified then source will be a .config made from\
defconfig set by the -d option (default = mvebu_v7_defconfig).

Example: 'diffdefconfig myconfig.config', result in diff_defconfig\
You can use the diff_defconfig file as follows:

cp arch/arm/configs/mvebu_v7_defconfig arch/arm/configs/merged_defconfig\
cat diffdef/diff_defconfig           >>arch/arm/configs/merged_defconfig\
make ARCH=arm merged_defconfig

The resulting .config will be the same as the original myconfig.config.

Example: 'diffdefconfig myconfig1.config myconfig2.config'

Compares .config files, list changes except kconfig's defaults.

