# KiCAD files of a SGMII PHY board with TI DP83867S

KiCAD files of a simple SGMII PHY

![print board](https://github.com/kazkojima/dp83867s-sgmii-board/blob/main/images/sgmphy-board.png)


It works with an ECP5 evaluation board LFE5UM5G-85F-EVN running [LiteX](https://github.com/enjoy-digital/litex).

![With LEF5UM5G-85G](https://github.com/kazkojima/dp83867s-sgmii-board/blob/main/images/sgmphy.png)

## Problems

* 1.0V LDO will be too hot when supplying 5V. It should be bigger package which has lower junction thermal resistance. 3.3V supply will be OK.

* SMA connectors were a bit too close to each other.

* REFCLK LDVS and CLKOUT outputs could be optional because almost MACs has their own CDR.

* Datasheet says "at minimum a 4-layer PCB should be used. However a 6-layer board is recommended." This 2-layer PCB violates it :-)
