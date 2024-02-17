cmake_minimum_required(VERSION 3.15)

juce_add_modules(
    ALIAS_NAMESPACE gin
    gin
    gin_dsp
    gin_graphics
    gin_gui
    gin_location
    gin_metadata
    gin_network
    gin_plugin
    gin_webp
    gin_simd
)
