cmake_minimum_required(VERSION 3.13.4)

project(SlicerCMF)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://cmf.slicer.org/")
set(EXTENSION_CATEGORY "SlicerCMF")
set(EXTENSION_CONTRIBUTORS "Lucia Cevidanes (University of Michigan), Beatriz Paniagua (Kitware), Jean-Christophe Fillion-Robin (Kitware)")
set(EXTENSION_DESCRIPTION "Dental image analysis to support patient-specific decision making and assessment of the disease progression via registration of serial images.")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/DCBIA-OrthoLab/SlicerCMF/master/SlicerCMF.png")
set(EXTENSION_SCREENSHOTURLS "http://www.example.com/Slicer/Extensions/SlicerCMF/Screenshots/1.png")
set(EXTENSION_DEPENDS
  BoneTextureExtension
  CMFreg
  EasyClip
  MeshToLabelMap
  MeshStatisticsExtension
  ModelToModelDistance
  PickAndPaintExtension
  Q3DC
  # ShapePopulationViewer
  # ShapeVariationAnalyzer
  # SPHARM-PDM
  ) # Specified as a list or 'NA' if any

# Not available as extension:
#  DatabaseInteractorExtension
#  GROUPS
#  MFSDA_Python

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(SlicerCMF)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})
