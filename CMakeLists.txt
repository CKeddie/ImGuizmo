
set(imguizmo_sources
    ${external}/ImGuizmo/GraphEditor.h   
    ${external}/ImGuizmo/GraphEditor.cpp 
    ${external}/ImGuizmo/ImGradient.h 
    ${external}/ImGuizmo/ImGradient.cpp   
    ${external}/ImGuizmo/ImSequencer.h   
    ${external}/ImGuizmo/ImSequencer.cpp 
    ${external}/ImGuizmo/ImCurveEdit.h   
    ${external}/ImGuizmo/ImCurveEdit.cpp  
    ${external}/ImGuizmo/ImGuizmo.h
    ${external}/ImGuizmo/ImGuizmo.cpp 
    ${external}/ImGuizmo/ImZoomSlider.h
)

add_library(ImGuizmo ${imguizmo_sources})
target_include_directories(ImGuizmo PUBLIC AFTER ${external}/ImGuizmo/)
set_target_properties(ImGuizmo PROPERTIES FOLDER "Dependencies/GUI")
target_link_libraries(ImGuizmo PUBLIC imgui)
