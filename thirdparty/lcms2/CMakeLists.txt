add_library(lcms2 STATIC
	lcms2/cmsintrp.c
	lcms2/cmsio0.c
	lcms2/cmsio1.c
	lcms2/cmslut.c
	lcms2/cmsmd5.c
	lcms2/cmsmtrx.c
	lcms2/cmsnamed.c
	lcms2/cmsopt.c
	lcms2/cmspack.c
	lcms2/cmspcs.c
	lcms2/cmsplugin.c
	lcms2/cmsps2.c
	lcms2/cmssamp.c
	lcms2/cmssm.c
	lcms2/cmsvirt.c
	lcms2/cmswtpnt.c
	lcms2/cmsxform.c
   )

set_target_properties(lcms2
      PROPERTIES
      COMPILE_FLAGS
            "-O2 -Wno-write-strings -ansi -Wnon-virtual-dtor -Woverloaded-virtual"
      )

include_directories(
      ${PROJECT_SOURCE_DIR}/thirdparty/lcms2/include
	#${PROJECT_SOURCE_DIR}/thirdparty/lcms2/src
      )
