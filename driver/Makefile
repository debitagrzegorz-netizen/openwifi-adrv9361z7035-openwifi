# Xianjun jiao. putaoshu@msn.com; xianjun.jiao@imec.be

obj-m += sdr.o openofdm_rx/openofdm_rx.o openofdm_tx/openofdm_tx.o tx_intf/tx_intf.o rx_intf/rx_intf.o xpu/xpu.o

# Test builds only: make OPENWIFI_LOCK_SANITY=1
# Warns if openwifi_tx returns with priv->lock still held and IRQs off.
ifeq ($(OPENWIFI_LOCK_SANITY),1)
ccflags-y += -DOPENWIFI_LOCK_SANITY
endif

all:
	make -C $(KDIR) M=$(PWD) modules
	# ARCH=arm CROSS_COMPILE=arm-linux-gnueabihf-

clean:
	rm -f *.ko *.o *.mod.o *.mod.c *.symvers *.order
