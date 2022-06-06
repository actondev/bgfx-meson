project('bgfx', 'cpp')

# credits: https://github.com/pminiszewski/bgfx-meson/blob/main/meson/bgfx/meson.build

bgfx_inc = include_directories([
  'include',
  '3rdparty/dxsdk/include',
  '3rdparty/khronos',
])

bgfx = library('bgfx',
               files(
                 # todo individual modules (d3d vs opengl vs html5 etc

                 # 'src/amalgamated.cpp',

                 'src/bgfx.cpp',
                 # 'src/debug_renderdoc.cpp',
                 'src/dxgi.cpp',
                 'src/glcontext_egl.cpp',
                 'src/glcontext_glx.cpp',
                 'src/glcontext_html5.cpp',
                 'src/glcontext_wgl.cpp',
                 'src/nvapi.cpp',
                 'src/renderer_agc.cpp',
                 'src/renderer_d3d11.cpp',
                 'src/renderer_d3d12.cpp',
                 'src/renderer_d3d9.cpp',
                 'src/renderer_gl.cpp',
                 'src/renderer_gnm.cpp',
                 'src/renderer_noop.cpp',
                 'src/renderer_nvn.cpp',
                 'src/renderer_vk.cpp',
                 'src/renderer_webgpu.cpp',
                 'src/shader.cpp',
                 'src/shader_dx9bc.cpp',
                 'src/shader_dxbc.cpp',
                 'src/shader_spirv.cpp',
                 'src/topology.cpp',
                 'src/vertexlayout.cpp',

               ), 
               include_directories: bgfx_inc,
               dependencies: [
                 dependency('gl'),
                 dependency('bx'),
                 dependency('bimg'),
                 ]
              )

bgfx_dep = declare_dependency(
  link_with: bgfx,
  include_directories: 'include'
)
