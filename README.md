# AIR-ROBOTICS
OUTCOMES: https://drive.google.com/drive/folders/1NxSlHTAYt0rh59rorZ9S8n7ySofK6pf2?usp=drive_link
Code Submission

Due to environment configuration issues on my new computer, I was unable to use Git for code submission. Instead, I have saved the complete implementation as a challenge.ipynb Jupyter notebook file for your review.


Code Explanation

PART 1 Solution Features:
Uses adaptive thresholding to handle variations in grassy backgrounds
Applies morphological operations to fill gaps in shapes
Filters noise based on contour area
Uses contour approximation to identify shape types
Calculates image moments to locate shape centers
Saves results to the specified directory

Optimization Approach & Key Methods
1. Color Space Conversion
HSV Color Space: Switched from BGR to HSV for more accurate color detection
Precise Color Ranges: Defined specific HSV ranges for bright/fluorescent colors
Increased Saturation/Value Thresholds (150-255) to target vibrant shapes

2. Noise Reduction Strategies
Morphological Operations: Applied closing and opening to clean up color masks
Area Filtering: Increased minimum area threshold to 2000 pixels to exclude grass patches
Circularity Check: Added circularity metric (>0.3) to filter out elongated grass shapes

4. Shape Recognition Improvements
Contour Approximation: Used polygon approximation for shape classification
Enhanced Circle Detection: Classified shapes with ≥8 sides as circles
Aspect Ratio Check: Differentiated squares from rectangles using bounding box ratios

5. User Experience Enhancements
Auto-Close Display: Window automatically closes after 2 seconds
Clear Labeling: Combined color and shape names in annotations
Return Value: Added processed image return for potential further processing

6. Robustness Features
Perimeter Validation: Added check to prevent division by zero
Error Handling: Included proper error messages for file loading issues
Directory Management: Automated output directory creation

Part 2 Solution Features (Optimized based on Problem 1):
Modular Design: Frame processing logic is encapsulated in the independent process_frame() function
Stream Processing: Processes video frame by frame, simulating a real-time processing environment
Progress Feedback: Displays processing progress for monitoring long-running operations
Result Saving: Saves processed video to the specified directory
Real-time Preview: Optionally displays real-time processing results
Resource Management: Properly handles opening and releasing of video resources
Optimizations and Improvements:
Code Reuse: Problem 2 reuses the core processing logic from Problem 1
Performance Considerations: Added progress feedback in video processing to prevent UI freezing
User Experience: Added keyboard control (q key to quit) and real-time preview
Robustness: Added error checking and resource cleanup
These two solutions provide simple yet effective methods for shape detection tasks in both static images and videos, laying the foundation for more complex tasks to follow. The results will be saved to the specified "F:\airrobotics" directory.


Part 5 (ROS2 Integration) Status:
I encountered memory allocation issues during ROS2 environment configuration that prevented implementation. After studying environment configuration methods and planning the implementation approach, I was unfortunately unable to resolve these hardware limitations in time for submission.

Part 6 (Enhanced Tracking) Concept:
My approach for advanced object tracking involves implementing reinforcement learning through multiple path simulations. This method would better fit motion pattern recognition by training the system to predict object movement trajectories even during occlusion periods, significantly improving tracking consistency in challenging scenarios.
