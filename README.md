Preface to the Invention:
I will introduce a method, do you understand whether you have the potential to become an AI recognition engineer.
Today, I will introduce a three-dimensional space recognition method to you. While some people may have discovered this method, within my knowledge, no individual or organization has publicly disclosed this technology. At present, AI 3D space recognition always aims to identify what the current object is and infer its spatial position from it. However, this method of the present invention only recognizes the features and positions of three-dimensional objects, infers what the objects look like, and then identifies what the three-dimensional objects are and what features they have. This recognition method solves the problem of incorrect recognition of three-dimensional and planar objects such as mirrors, water surfaces, and drawn images in one go. This method is based on the reference plane to identify whether the three-dimensional space is highly convex or concave relative to the reference plane. At least this method is clever and provides a different idea for everyone. Today, the principle and method are publicly available for anyone to learn.

Reason for reasoning:

In the process of invention, humans hope to infer a theorem or formula from objective laws, but it seems that it is not ideal for three-dimensional space recognition. At present, this invention can only infer objective laws, and my ability and financial resources are limited, so I am unable to derive theorems or formulas from it. I hope that talented colleagues can participate in the discussion, criticize and guide me.

The following only applies reasoning analysis to objective laws:

1、 The ideal core hardware device for this method is:

1. Camera: Adopting binocular cameras (i.e. dual cameras)
2. Gyroscope: (not discussed in this example)
3. Motor: Designed to mimic human eye rotation
(1) Horizontal direction: Free rotation within a controllable angle range, supporting simultaneous focusing of the left and right camera lens centers on objects
(2) Vertical direction: In a certain angle direction, the left and right cameras can be controlled to rotate synchronously and in the same direction
4. Can be focused, preferably with focus value data available (optional).
5. Following the principle of human eyes, use the interval focusing method during each blink interval

2、 Principles of 3D space recognition:
Based on existing hardware, multiple or several mutually supportive algorithm methods can be used (such as: 1. Front and rear frame comparison recognition method; 2. Left and right frame comparison recognition method; 3. Convolutional neural recognition, 4. Focus distance method) to ensure the reliability of recognition.

3、 Identification process:

1. The acquisition of three-dimensional (3D) spatial image data by binocular cameras generates two-dimensional (2D) images, so our core focus is to infer the high convexity and low concavity characteristics of three-dimensional spatial objects based on objective laws of two-dimensional pixel data.
Identify the change status of pixels between the current frame and the frame at the previous time point in three-dimensional space
Identify the change status of pixels between the current frame and the previous two time points in three-dimensional space,
Based on the characteristics of pixel changes before and after, identify whether the three-dimensional space is high convex or low concave relative to the reference plane, save it as three view data, and perform reference plane point (feature annotation) data, high convex stereo point (feature annotation) data, and low concave stereo point (feature annotation) data on the image pixel data.

2. Use the pixel comparison method between the current frame and the previous frame, or one of the previous frames. (Note: The previous frame and the previous few frames mentioned in this sentence refer to the calculation using the time interval method. In reality, the previous frame may refer to one of the previous frames.)

3. Save the current point (feature annotation) recognition three-dimensional space as image data and mark the feature attributes.

4. After analyzing the characteristics of the current three-dimensional object, establish three view data for future feature recognition or memory exchange learning.

5. When the left and right cameras are in a stationary state or in a moving state, the current left and right frame data obtained by synchronously focusing on a certain object can be analyzed. Based on the distance interval between the left and right cameras, trigonometric functions, and horizontal imaging principles, the feature analysis of the image data collected at the same time can determine whether the current object is a highly convex object.

4、 Specific algorithm steps:

1. Dynamic state (better for three-dimensional spatial state features):
Single camera front back frame comparison method: After the camera moves horizontally forward, within a certain time interval of movement, the front and back frames will produce feature changes. The horizontal plane is different from the high convex stereo, and the horizontal plane is different from the low concave stereo. After the camera collects two-dimensional image data, the displacement and stretching data are different. This method can recognize the features of three-dimensional space;

2. Static state (better for identifying individual objects in three-dimensional space):
Comparison method of synchronized data frame acquisition by binocular cameras:
Using left and right cameras to collect positional difference data, calculate the three-dimensional spatial feature changes of the object through trigonometric functions and special data offset values

A、 Analysis of objects directly in front
As the camera moves forward, the object being captured in front will also experience displacement. However, the horizontal plane moves at the same speed, but the captured image features change according to a specific pattern, resulting in visual stretching; However, the displacement of highly convex objects is different from that of the horizontal plane. Highly convex objects are slower than the horizontal plane, and the changes in the collected images are not obvious in the distance. The changes in the objects in front of us are more obvious than those in the horizontal plane, and the changes are accelerated.

B、 Analysis of objects on the left and right sides
As the camera moves forward,

High convex objects on the left and right sides, whether they move vertically or not with displacement;

Horizontal objects on the left and right sides will change their angle and direction vertically with displacement;
