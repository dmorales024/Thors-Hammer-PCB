
FROM zephyrprojectrtos/ci
WORKDIR /root



COPY . .
COPY prj.conf .
RUN west init -m https://github.com/nrfconnect/sdk-nrf --mr v2.4.2
RUN west update
RUN west build --build-dir $(pwd)/c-programming-lab/build $(pwd)/c-programming-lab --pristine --board nrf52833dk_nrf52833 --no-sysbuild -- -DNCS_TOOLCHAIN_VERSION=NONE -DCONF_FILE=$(pwd)/c-programming-lab/prj.conf
