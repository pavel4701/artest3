<!doctype HTML>
<html>
    <head>
        <meta name="viewport" content="width=device-width, user-scalable=no, minimum-scale=1.0, maximum-scale=1.0">
    </head>
    <script src="https://aframe.io/releases/0.9.0/aframe.min.js"></script>
    <script src="https://rawgit.com/jeromeetienne/AR.js/master/aframe/build/aframe-ar.min.js"></script>
    <script src="https://rawgit.com/donmccurdy/aframe-extras/master/dist/aframe-extras.loaders.min.js"></script>
    
    <body style='margin : 0px; overflow: hidden;'>
        <!-- we add detectionMode and matrixCodeType to tell AR.js to recognize barcode markers -->
        <a-scene embedded arjs='sourceType: webcam; debugUIEnabled: false; detectionMode: mono_and_matrix; matrixCodeType: 3x3;'>

        <a-assets>
            <a-asset-item id="animated-asset" src="https://raw.githubusercontent.com/nicolocarpignoli/nicolocarpignoli.github.io/master/ar-playground/models/CesiumMan.gltf"></a-asset-item>
        </a-assets>

        <a-marker type='barcode' value='7'>
        <a-assets>
            <a-asset-item id="tree-model" src="https://raw.githubusercontent.com/pavel4701/pattern-marker./master/kok2.dae" crossOrigin="anonymous"></a-asset-item>
            <a-asset-item id="text-model" src="https://raw.githubusercontent.com/pavel4701/pattern-marker./master/kok.dae" crossOrigin="anonymous"></a-asset-item>
       </a-assets>
        </a-marker>

        <a-marker id="animated-marker" type='barcode' value='6'>
        <a-assets>
            <a-asset-item id="tree-model" src="https://raw.githubusercontent.com/pavel4701/pattern-marker./master/kok2.dae" crossOrigin="anonymous"></a-asset-item>
            <a-asset-item id="text-model" src="https://raw.githubusercontent.com/pavel4701/pattern-marker./master/kok.dae" crossOrigin="anonymous"></a-asset-item>
       </a-assets>
        </a-marker>

        <!-- use this <a-entity camera> to support multiple-markers, otherwise use <a-marker-camera> instead of </a-marker> -->
        <a-entity camera></a-entity>
        </a-scene>
    </body>
</html>
