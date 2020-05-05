filegroup (
    name = "python-bin",
    srcs = ["python374/bin/python3.7"],
    visibility = ["//visibility:public"],
)

filegroup (
    name = "python-files",
    srcs = glob([
        "python374/**/*",
    ]),
    visibility = ["//visibility:public"],
)

py_runtime(
    name = "python-3.7.4",
    files = glob(
        include = [
            ":python-files"
        ],
        exclude = [
            "python374/lib/cmake/**",
            "python374/lib/pkgconfig/**",
            "python374/lib/python3.7/site-packages/setuptools/command/launcher manifest.xml",
            "python374/lib/python3.7/site-packages/setuptools/script (dev).tmpl",
            "python374/lib/terminfo/**",
        ],
    ),
    interpreter = "python374/bin/python3.7",
    visibility = ["//visibility:public"],
)