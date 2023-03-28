import 'dart:ui';

import 'package:flutter/cupertino.dart';

class MyCustomeClass extends CustomClipper<Path>{
  @override
  Path getClip(Size size) {
    Path path = Path();
  path.lineTo(0, size.height/2);
   // path.quadraticBezierTo(size.width/2, size.height, size.width, size.height/2);
    path.quadraticBezierTo(size.width*0.2, size.height, size.width/2,size.height*0.7);
    path.quadraticBezierTo(size.width*0.8, size.height/3, size.width, size.height);
    path.lineTo(size.width, 0);
    path.close();
    return path;

  }

  @override
  bool shouldReclip(covariant CustomClipper<Path> oldClipper) {
    // TODO: implement shouldReclip
    throw UnimplementedError();
  }

}