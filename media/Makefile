TARGET=Textures.xbt
XBMCTEX=/build/buildd/xbmc-13.0~git20130901.0828-alpha7/tools/TexturePacker/TexturePacker

IMAGES := $(shell find . -name "*jpg")
IMAGES += $(shell find . -name "*png")
IMAGES += $(shell find . -name "*gif")

all: $(TARGET)

.PHONY: force

$(TARGET): $(XBMCTEX) $(IMAGES)
ifeq (,1)
	$(XBMCTEX) -use_none -input . -output $(TARGET)
else
	$(XBMCTEX) -input . -output $(TARGET)

endif
$(XBMCTEX): force
	$(MAKE) -C /build/buildd/xbmc-13.0~git20130901.0828-alpha7/tools/TexturePacker

clean:
	rm -f $(TARGET)
distclean: clean

