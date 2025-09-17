# The Static Spin Illusion

This project introduces a novel method for transforming static two-dimensional images into captivating three-dimensional spinning motion illusions. By leveraging phase-shifted filters and AI-generated depth maps, we can create the perception of depth and movement in a static image.

---

## How it Works

The core of this technique is the combination of several image processing and computer vision concepts:

1.  **Image Pre-processing**: The input image is rotated to a horizontal orientation and converted to grayscale to focus on luminance-based edge structures.
2.  **Depth Map Generation**: A zero-shot depth estimator, **Marigold**, is used to create an initial depth map. This map is then enhanced to improve the representation of near-field depth variations.
3.  **Quadrature Filter Implementation**: We use a pair of oriented quadrature filters—a second derivative Gaussian filter ($G_2$) and its Hilbert transform ($H_2$)—to isolate and manipulate the edges in the image. To prevent aliasing, a Sobel filter is applied before the Hilbert transformation.
4.  **Phase Modulation and Motion Synthesis**: The final illusion is created by temporally varying the phase of the filtered images. The perceived speed and direction of the spinning motion are dynamically altered for each pixel based on its depth value, which creates a compelling three-dimensional effect.

---

## Demonstration

Check out the video below to see the static spin illusion in action:

[http://www.youtube.com/watch?v=SPNykV3BV8E](http://www.youtube.com/watch?v=SPNykV3BV8E)

---

