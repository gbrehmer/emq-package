deb: clean package

prepare:
	mkdir -p emqttd-${EMQ_VERSION}
	git clone -b package https://github.com/gbrehmer/emq-relx.git emqttd-${EMQ_VERSION}
	cp debian -r emqttd-${EMQ_VERSION}/
	cd emqttd-${EMQ_VERSION} && dpkg-buildpackage -us -uc && rm -rf ../debian && mv debian/ ../

package: prepare
	mkdir ../package
	cp emqttd_${EMQ_VERSION}_*.deb ../package
	rm -rf emqttd*
clean:
	rm -rf emqttd*
