#Kernel GPS (Zubax GNSS 2)
![](/assets/Zubax GNSS 2 - Titan Elite 3 copy-500x500.jpg)

While any UAVCAN supporting GPS/GNSS can be used, we offer the reliable and high quality Zubax GNSS 2 as an optional accessory on our store. With this GPS unit plugged into Kernel (individual cameras and arrays) you will get automatic geo-tagging to each captured image.

Purchase Zubax GNSSS 2 on MAPIR store
[Zubax GNSS 2 DATASHEET](https://files.zubax.com/products/com.zubax.gnss/Zubax_GNSS_2_Datasheet.pdf)
[Zubax manufacturer website for GNSS 2 unit](https://shop.titaneliteinc.com/index.php?route=product/product&search=zubax%20gnss&product_id=987)


##Configuring Zubax GNSS 2 For Direct Camera Geo-Tagging

When you purchase the Zubax GNSS 2 from our MAPIR store, we have already changed the UAVCAN Node ID to a value of 5 (defualt is 0) so that you can connect the GNSS directly to Kernel. If you are connecting the GNSS to an autopilot such as the Pixhawk (2/1) you will want to change it back to 0 by following the below directions. The autopilot will dynamically assign it a node ID. If you have purchased the Zubax GNSS 2 from a different supplier, then use the below information to change the Node ID value to something other than the default (0) or Kernel's default value (16).


