set(external_root ${CMAKE_CURRENT_SOURCE_DIR})

set(imguizmo_sources
    ${external_root}/GraphEditor.h   
    ${external_root}/GraphEditor.cpp 
    ${external_root}/ImGradient.h 
    ${external_root}/ImGradient.cpp   
    ${external_root}/ImSequencer.h   
    ${external_root}/ImSequencer.cpp 
    ${external_root}/ImCurveEdit.h   
    ${external_root}/ImCurveEdit.cpp  
    ${external_root}/ImGuizmo.h
    ${external_root}/ImGuizmo.cpp 
    ${external_root}/ImZoomSlider.h
)

add_library(ImGuizmo STATIC ${imguizmo_sources})
target_include_directories(ImGuizmo PUBLIC ${external_root})
set_target_properties(ImGuizmo PROPERTIES FOLDER "Dependencies/GUI")
