<h2>README for mbed TLS with MILAGRO</h2>

Milagro TLS  has only been built and tested on Linux and Mac with the GCC tool chain.

First install the mpin-crypto library and then the mbed TLS library.

CMake is required to build the library and can usually be installed from
the operating system package manager. 

<ul type="disc">
  <li>sudo apt-get install cmake</li>
</ul>

If not, then you can download it from www.cmake.org


<h2>Compiling mpin-crypto-c</h2>

# # clone milagro-crypto-c, pay attention on cloning the develop branch
- git clone https://github.com/miracl/milagro-crypto-c.git
- cd milagro-crypto-c
- mkdir release
- cd release
- cmake -D CMAKE_INSTALL_PREFIX=/opt/amcl -D USE_ANONYMOUS=on -D WORD_LENGTH=64 -D BUILD_WCC=on  -D BUILD_MPIN=on  ..
- make
- make test
- sudo make install


<h2>Compiling mbedtls</h2>

- git clone https://github.com/miracl/mbedtls.git
- cd mtls
- mkdir release
- cd release
- cmake -D AMCL_INSTALL_DIR=/opt/amcl ..
- make
- make test
- sudo make install

