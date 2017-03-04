project(protobuf)
cmake_minimum_required(VERSION 3.0)

set(protobuf_source_dir ${CMAKE_CURRENT_SOURCE_DIR})
set(libprotobuf_lite_files
  ${protobuf_source_dir}/src/google/protobuf/arena.cc
  ${protobuf_source_dir}/src/google/protobuf/arenastring.cc
  ${protobuf_source_dir}/src/google/protobuf/extension_set.cc
  ${protobuf_source_dir}/src/google/protobuf/generated_message_util.cc
  ${protobuf_source_dir}/src/google/protobuf/io/coded_stream.cc
  ${protobuf_source_dir}/src/google/protobuf/io/zero_copy_stream.cc
  ${protobuf_source_dir}/src/google/protobuf/io/zero_copy_stream_impl_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/message_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/repeated_field.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/atomicops_internals_x86_gcc.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/atomicops_internals_x86_msvc.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/bytestream.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/common.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/int128.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/once.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/status.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/statusor.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/stringpiece.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/stringprintf.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/structurally_valid.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/strutil.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/time.cc
  ${protobuf_source_dir}/src/google/protobuf/wire_format_lite.cc
)

set(libprotobuf_files
  ${protobuf_source_dir}/src/google/protobuf/any.cc
  ${protobuf_source_dir}/src/google/protobuf/any.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/api.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/importer.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/parser.cc
  ${protobuf_source_dir}/src/google/protobuf/descriptor.cc
  ${protobuf_source_dir}/src/google/protobuf/descriptor.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/descriptor_database.cc
  ${protobuf_source_dir}/src/google/protobuf/duration.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/dynamic_message.cc
  ${protobuf_source_dir}/src/google/protobuf/empty.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/extension_set_heavy.cc
  ${protobuf_source_dir}/src/google/protobuf/field_mask.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/generated_message_reflection.cc
  ${protobuf_source_dir}/src/google/protobuf/io/gzip_stream.cc
  ${protobuf_source_dir}/src/google/protobuf/io/printer.cc
  ${protobuf_source_dir}/src/google/protobuf/io/strtod.cc
  ${protobuf_source_dir}/src/google/protobuf/io/tokenizer.cc
  ${protobuf_source_dir}/src/google/protobuf/io/zero_copy_stream_impl.cc
  ${protobuf_source_dir}/src/google/protobuf/map_field.cc
  ${protobuf_source_dir}/src/google/protobuf/message.cc
  ${protobuf_source_dir}/src/google/protobuf/reflection_ops.cc
  ${protobuf_source_dir}/src/google/protobuf/service.cc
  ${protobuf_source_dir}/src/google/protobuf/source_context.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/struct.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/mathlimits.cc
  ${protobuf_source_dir}/src/google/protobuf/stubs/substitute.cc
  ${protobuf_source_dir}/src/google/protobuf/text_format.cc
  ${protobuf_source_dir}/src/google/protobuf/timestamp.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/type.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/unknown_field_set.cc
  ${protobuf_source_dir}/src/google/protobuf/util/field_comparator.cc
  ${protobuf_source_dir}/src/google/protobuf/util/field_mask_util.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/datapiece.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/default_value_objectwriter.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/error_listener.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/field_mask_utility.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/json_escaping.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/json_objectwriter.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/json_stream_parser.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/object_writer.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/proto_writer.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/protostream_objectsource.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/protostream_objectwriter.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/type_info.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/type_info_test_helper.cc
  ${protobuf_source_dir}/src/google/protobuf/util/internal/utility.cc
  ${protobuf_source_dir}/src/google/protobuf/util/json_util.cc
  ${protobuf_source_dir}/src/google/protobuf/util/message_differencer.cc
  ${protobuf_source_dir}/src/google/protobuf/util/time_util.cc
  ${protobuf_source_dir}/src/google/protobuf/util/type_resolver_util.cc
  ${protobuf_source_dir}/src/google/protobuf/wire_format.cc
  ${protobuf_source_dir}/src/google/protobuf/wrappers.pb.cc
)

set(libprotoc_files
  ${protobuf_source_dir}/src/google/protobuf/compiler/code_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/command_line_interface.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_enum.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_enum_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_extension.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_file.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_helpers.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_map_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_message.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_message_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_primitive_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_service.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/cpp/cpp_string_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_doc_comment.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_enum.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_enum_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_field_base.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_helpers.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_map_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_message.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_message_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_primitive_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_reflection_class.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_repeated_enum_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_repeated_message_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_repeated_primitive_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_source_generator_base.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/csharp/csharp_wrapper_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_context.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_doc_comment.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_enum.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_enum_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_enum_field_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_enum_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_extension.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_extension_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_file.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_generator_factory.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_helpers.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_lazy_message_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_lazy_message_field_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_map_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_map_field_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_message.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_message_builder.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_message_builder_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_message_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_message_field_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_message_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_name_resolver.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_primitive_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_primitive_field_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_service.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_shared_code_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_string_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/java/java_string_field_lite.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_enum.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_enum_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_extension.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_file.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_helpers.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_map_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_message.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_message_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/javanano/javanano_primitive_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/js/js_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/js/well_known_types_embed.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_enum.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_enum_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_extension.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_file.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_helpers.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_map_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_message.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_message_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_oneof.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/objectivec/objectivec_primitive_field.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/php/php_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/plugin.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/plugin.pb.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/python/python_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/ruby/ruby_generator.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/subprocess.cc
  ${protobuf_source_dir}/src/google/protobuf/compiler/zip_writer.cc
)

set(js_well_known_types_sources,
  ${protobuf_source_dir}/src/google/protobuf/compiler/js/well_known_types/any.js
  ${protobuf_source_dir}/src/google/protobuf/compiler/js/well_known_types/struct.js
  ${protobuf_source_dir}/src/google/protobuf/compiler/js/well_known_types/timestamp.js
)
add_executable(js_embed ${protobuf_source_dir}/src/google/protobuf/compiler/js/embed.cc)
add_custom_command(
  OUTPUT ${protobuf_source_dir}/src/google/protobuf/compiler/js/well_known_types_embed.cc
  DEPENDS js_embed ${js_well_known_types_sources}
  COMMAND js_embed ${js_well_known_types_sources} > ${protobuf_source_dir}/src/google/protobuf/compiler/js/well_known_types_embed.cc
)

set(protoc_files
  ${protobuf_source_dir}/src/google/protobuf/compiler/main.cc
)

add_library(protobuf STATIC ${libprotobuf_files} ${libprotobuf_lite_files})
target_include_directories(protobuf PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)

add_executable(protoc ${protoc_files} ${libprotoc_files})
target_include_directories(protoc PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src)
target_link_libraries(protoc PRIVATE protobuf)

find_package(Threads REQUIRED)
if(CMAKE_USE_PTHREADS_INIT)
  target_compile_definitions(protobuf PRIVATE HAVE_PTHREAD)
  target_compile_definitions(protoc PRIVATE HAVE_PTHREAD)
endif()

if(MSVC)
  target_compile_options(protobuf PRIVATE /MP /bigobj)
  target_compile_options(protobuf PRIVATE /wd4244 /wd4267 /wd4018 /wd4355 /wd4800 /wd4251 /wd4996 /wd4146 /wd4305)
  target_compile_options(protoc PRIVATE /MP /bigobj)
  target_compile_options(protoc PRIVATE /wd4244 /wd4267 /wd4018 /wd4355 /wd4800 /wd4251 /wd4996 /wd4146 /wd4305)
endif()

set_target_properties(protoc PROPERTIES PATH ${CMAKE_CURRENT_BINARY_DIR}/protoc)

if(${CMAKE_CURRENT_SOURCE_DIR} STREQUAL ${CMAKE_SOURCE_DIR})
  set(CMAKE_INSTALL_PREFIX ${CMAKE_CURRENT_BINARY_DIR}/install)
  install(TARGETS protobuf DESTINATION lib)
  install(TARGETS protoc DESTINATION bin)
  install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/src/google DESTINATION include FILES_MATCHING PATTERN "*.h")
endif()
