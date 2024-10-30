# Target platform

platform(
	name = "toolchain_arm64_gcc_docker",
	constraint_values = [
		"@platforms//cpu:arm64",
	],
)

# Execution platform

constraint_setting(
	name = "docker_image"
)

constraint_value(
	name = "docker_image_linux_arm64",
	constraint_setting = ":docker_image",
    visibility = ["//visibility:public"],
)

platform(
	name = "execution_platform",
	constraint_values = [
		":docker_image_linux_arm64",
	],
	exec_properties = {
		"container-image": "docker://docker.io/dockcross/linux-arm64:20230421-a0eaff4",
	},
)
