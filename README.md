# Hello-World
aidl_interface {
    name: "my-aidl",
    srcs: ["srcs/aidl/**/*.aidl"],
    local_include_dir: "srcs/aidl",
    imports: ["other-aidl"],
    versions_with_info: [
        {
            version: "1",
            imports: ["other-aidl-V1"],
        },
        {
            version: "2",
            imports: ["other-aidl-V3"],
        }
    ],
    stability: "vintf",
    backend: {
        java: {
            enabled: true,
            platform_apis: true,
        },
        cpp: {
            enabled: true,
        },
        ndk: {
            enabled: true,
        },
        rust: {
            enabled: true,
        },
    },

}

