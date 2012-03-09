SCSS3 is a crossbrowser SASS implementation of CSS3 properties.

In short, instead of doing this::

    .test-border-radius {
        -webkit-border-radius: 12px; /* Saf3-4, iOS 1-3.2, Android ≤1.6 */
        -moz-border-radius: 12px; /* FF1-3.6 */
        border-radius: 12px; /* Opera 10.5, IE9, Saf5, Chrome, FF4, iOS 4, Android 2.1+ */
        -moz-background-clip: padding; 
        -webkit-background-clip: padding-box; 
        background-clip: padding-box;
    }


It allows you to simply do this::

    @import "css3.scss";

    .test-border-radius {
        @include border-radius(10px, 10px, 0, 0);
    }

Currently the following mixin are supported:

 * border-radius
 * opacity
 * box-shadow
 * background-gradient
 * rotate
 * scale
 * transform-3d
 * transition
 * background-size
 * box-column
 * tab-size

 The following class are also provided for extension:

  * .clearfix
  * .reset-box

Credits
=======

This project was created and is sponsored by:

.. figure:: http://motion-m.ca/media/img/logo.png
    :figwidth: image

Motion Média (http://motion-m.ca)