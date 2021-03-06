# $FreeBSD$

PORTNAME=	cargo-tree
DISTVERSION=	0.28.0
PORTREVISION=	2
CATEGORIES=	devel
MASTER_SITES=	CRATESIO
DISTFILES=	${DISTNAME}${EXTRACT_SUFX}

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Rust's cargo subcommand to visualize dependency graph as a tree #'

LICENSE=	APACHE20 MIT
LICENSE_COMB=	dual
LICENSE_FILE_APACHE20=	${WRKSRC}/LICENSE-APACHE
LICENSE_FILE_MIT=	${WRKSRC}/LICENSE-MIT

LIB_DEPENDS=	libcurl.so:ftp/curl \
		libgit2.so:devel/libgit2 \
		libssh2.so:security/libssh2

USES=		cargo ssl

CARGO_CRATES=	adler32-1.0.4 \
		aho-corasick-0.7.6 \
		ansi_term-0.11.0 \
		atty-0.2.13 \
		autocfg-0.1.7 \
		backtrace-0.3.40 \
		backtrace-sys-0.1.32 \
		bitflags-1.2.1 \
		bstr-0.2.8 \
		bytesize-1.0.0 \
		c2-chacha-0.2.3 \
		cargo-0.41.0 \
		cargo-platform-0.1.0 \
		cc-1.0.48 \
		cfg-if-0.1.10 \
		clap-2.33.0 \
		commoncrypto-0.2.0 \
		commoncrypto-sys-0.2.0 \
		core-foundation-0.6.4 \
		core-foundation-sys-0.6.2 \
		crates-io-0.29.0 \
		crc32fast-1.2.0 \
		crossbeam-channel-0.3.9 \
		crossbeam-utils-0.6.6 \
		crypto-hash-0.3.4 \
		curl-0.4.25 \
		curl-sys-0.4.24 \
		env_logger-0.7.1 \
		failure-0.1.6 \
		failure_derive-0.1.6 \
		filetime-0.2.8 \
		fixedbitset-0.1.9 \
		flate2-1.0.13 \
		fnv-1.0.6 \
		foreign-types-0.3.2 \
		foreign-types-shared-0.1.1 \
		fs2-0.4.3 \
		fwdansi-1.1.0 \
		getrandom-0.1.13 \
		git2-0.10.2 \
		git2-curl-0.11.0 \
		glob-0.3.0 \
		globset-0.4.4 \
		heck-0.3.1 \
		hermit-abi-0.1.5 \
		hex-0.3.2 \
		hex-0.4.0 \
		home-0.5.1 \
		humantime-1.3.0 \
		idna-0.2.0 \
		ignore-0.4.10 \
		im-rc-13.0.0 \
		itoa-0.4.4 \
		jobserver-0.1.17 \
		lazy_static-1.4.0 \
		lazycell-1.2.1 \
		libc-0.2.66 \
		libgit2-sys-0.9.2 \
		libnghttp2-sys-0.1.2 \
		libssh2-sys-0.2.13 \
		libz-sys-1.0.25 \
		log-0.4.8 \
		matches-0.1.8 \
		memchr-2.2.1 \
		miniz_oxide-0.3.5 \
		miow-0.3.3 \
		num_cpus-1.11.1 \
		opener-0.4.1 \
		openssl-0.10.26 \
		openssl-probe-0.1.2 \
		openssl-sys-0.9.53 \
		ordermap-0.3.5 \
		percent-encoding-2.1.0 \
		petgraph-0.4.13 \
		pkg-config-0.3.17 \
		ppv-lite86-0.2.6 \
		proc-macro-error-0.2.6 \
		proc-macro2-1.0.6 \
		quick-error-1.2.2 \
		quote-1.0.2 \
		rand-0.7.2 \
		rand_chacha-0.2.1 \
		rand_core-0.5.1 \
		rand_hc-0.2.0 \
		redox_syscall-0.1.56 \
		regex-1.3.1 \
		regex-syntax-0.6.12 \
		remove_dir_all-0.5.2 \
		rustc-demangle-0.1.16 \
		rustc-workspace-hack-1.0.0 \
		rustc_version-0.2.3 \
		rustfix-0.4.6 \
		ryu-1.0.2 \
		same-file-1.0.5 \
		schannel-0.1.16 \
		scopeguard-1.0.0 \
		semver-0.9.0 \
		semver-parser-0.7.0 \
		serde-1.0.104 \
		serde_derive-1.0.104 \
		serde_ignored-0.1.1 \
		serde_json-1.0.44 \
		shell-escape-0.1.4 \
		sized-chunks-0.3.1 \
		smallvec-1.1.0 \
		socket2-0.3.11 \
		strip-ansi-escapes-0.1.0 \
		strsim-0.8.0 \
		structopt-0.3.5 \
		structopt-derive-0.3.5 \
		syn-1.0.11 \
		synstructure-0.12.3 \
		tar-0.4.26 \
		tempfile-3.1.0 \
		termcolor-1.0.5 \
		textwrap-0.11.0 \
		thread_local-0.3.6 \
		toml-0.5.5 \
		typenum-1.11.2 \
		unicode-bidi-0.3.4 \
		unicode-normalization-0.1.11 \
		unicode-segmentation-1.6.0 \
		unicode-width-0.1.7 \
		unicode-xid-0.2.0 \
		url-2.1.0 \
		utf8parse-0.1.1 \
		vcpkg-0.2.8 \
		vec_map-0.8.1 \
		vte-0.3.3 \
		walkdir-2.2.9 \
		wasi-0.7.0 \
		winapi-0.3.8 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.2 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		wincolor-1.0.2

PLIST_FILES=	bin/${PORTNAME}

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/cargo-tree

.include <bsd.port.mk>
