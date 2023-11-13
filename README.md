<h1>Watermarking digital images using steganography</h1>
<p>Digital Steganography process of embedding an invisible signature into the image, which can be used to prove the authenticity of the image and track its ownership.
A popular steganogrphy tenchnique using Least Significant Bit(LSB) insertion.In the LSB method, the least significant bit of each pixel in the host image is replaced with the corresponding bit of the watermark image. This method is easy to implement and provides good visual quality. Information is hidden in the least significant bits of a pixel or sample. This is because the modifications are subtle and difficult to detect using the naked eye</p>
<br>
<h2>Implemantation</h2>
<p>The detailed implementation of the algorithm is describe below:</p>
<ul>
  <li>The algorithm reads an image file</li>
  <li> A secret file containing the watermark is read and its contents are converted to binary</li>
  <li>The size of image is determined by getting the number of rows and number of columns</li>
  <li>A colored image contains three color channels (red, green, blue). The algorithm loops through each pixel in the pixel, replacing the least significant bit of each color channel with a bit from a secret channel. This is repeated until the entire secret message (watermark) is is hidden or the end of the image is reached.</li>
  <li>The modified data is written to a new file to create a new image</li>
</ul>
<p>To verify the watermark:</p>
<ul>
  <li>The embedded image is read</li>
  <li>The size of the image is determined by getting the number of rows and columns</li>
  <li>A variable is initialized to store the message</li>
  <li>The algorithm loops through the entire image. As it loops through the image, the LSB of each color channel of a each pixel is written to the initialized variable</li>
  <li>This continues until the entire watermark has been decoded or the end of the image is reached</li>
  <li>The decoded data in the initialized variable is converted from binary to string and compared with the original </li>
</ul>
