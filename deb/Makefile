deb: clean package

prepare:
	mkdir -p emqttd-${EMQ_VERSION} 
	git clone -b v${EMQ_VERSION}-agrotis https://github.com/sulzbach/emqx-rel emqttd-${EMQ_VERSION}
	cp debian -r emqttd-${EMQ_VERSION}/
	cd emqttd-${EMQ_VERSION} && dpkg-buildpackage -us -uc && rm -rf ../debian && mv debian/ ../

package: prepare
	mkdir -p ../package
	cp emqttd_*.deb ../package
	rm -rf emqttd*
clean:
	rm -rf emqttd*
