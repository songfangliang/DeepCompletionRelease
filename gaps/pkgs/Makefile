#
# Makefile for GAPS pkgs
#


# 
# Library file names
#

ARCH=$(shell uname -m)
LIB_DIR=../lib/$(ARCH)
LIB=$(LIB_DIR)/libgaps.a
PKG_LIBS= \
  $(LIB_DIR)/libR2Shapes.a \
  $(LIB_DIR)/libRNMath.a \
  $(LIB_DIR)/libRNBasics.a \
  $(LIB_DIR)/libCSparse.a \
  $(LIB_DIR)/libjpeg.a \
  $(LIB_DIR)/libpng.a


# 
# Make targets
#

opt:
	$(MAKE) target "TARGET=$@"
	rm -f $(LIB)
	ar ur $(LIB) $(PKG_LIBS)

debug:
	$(MAKE) target "TARGET=$@"
	rm -f $(LIB)
	ar ur $(LIB) $(PKG_LIBS)

mesa:
	$(MAKE) target "TARGET=$@"

clean:
	$(MAKE) target "TARGET=$@"

target: 
	cd RNBasics; $(MAKE) $(TARGET)
	cd RNMath; $(MAKE) $(TARGET)
	cd R2Shapes; $(MAKE) $(TARGET)
	cd CSparse; $(MAKE) $(TARGET)
	cd jpeg; $(MAKE) $(TARGET)
	cd png; $(MAKE) $(TARGET)





