Leaflet.WMS.GetLegendGraphic
============================

Simple little function to add a new function to Leaflet.WMS to fetch the layer's legend graphic.

After including this plugin all Leaflet.WMS will have a new function named getLegendGraphic(). 

In order to support layers made with with multiple WMS layers getLegendGraphic() returns a hash where the 
key is the individual layer name and the value is the URL for the legend.

getLegendGraphic accepts an optional hash of arguments. The default request parameters 
are extended with the argument hash. The hash is passed to L.Util.getParamString and used
in the URL's query string.

    {
      'LAYER'   : this.wmsParams.layers,
      'REQUEST' : 'GetLegendGraphic',
      'VERSION' : this.wmsParams.version,
      'FORMAT'  : this.wmsParams.format,
      'WIDTH'   : 20,
      'HEIGHT'  : 20
    }
