include(${QT_USE_FILE})
set(qgit_SRCS
annotate.cpp
cache.cpp
commitimpl.cpp
consoleimpl.cpp
customactionimpl.cpp
dataloader.cpp
domain.cpp
exceptionmanager.cpp
filecontent.cpp
filelist.cpp
fileview.cpp
git.cpp
git_startup.cpp
lanes.cpp
listview.cpp
mainimpl.cpp
myprocess.cpp
namespace_def.cpp
patchcontent.cpp
patchview.cpp
qgit.cpp
rangeselectimpl.cpp
revdesc.cpp
revsview.cpp
settingsimpl.cpp
smartbrowse.cpp
treeview.cpp
)
qt4_automoc(${qgit_SRCS})
SET(qgit_UIS
commit.ui
console.ui
customaction.ui
fileview.ui
help.ui
mainview.ui
patchview.ui
rangeselect.ui
revsview.ui
settings.ui
)
QT4_WRAP_UI(qgit_UIS_H ${qgit_UIS})
include_directories(${CMAKE_CURRENT_BINARY_DIR})
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
add_executable(qgit ${qgit_SRCS} ${qgit_UIS_H} )
target_link_libraries(qgit ${QT_LIBRARIES})
install(TARGETS qgit DESTINATION bin)

