# $FreeBSD: head/sysutils/terraform/Makefile 520926 2019-12-26 15:43:22Z lifanov $

PORTNAME=	terraform
PORTVERSION=	0.12.24
DISTVERSIONPREFIX=	v

CATEGORIES=	sysutils

MAINTAINER=	lifanov@FreeBSD.org
COMMENT=	Provides a common configuration to launch infrastructure

LICENSE=	MPL20
LICENSE_FILE=	${WRKSRC}/LICENSE

USE_GITHUB=	yes
GH_ACCOUNT=	hashicorp

PLIST_FILES=	bin/${PORTNAME}

USES=	go:modules

post-patch:
	${REINPLACE_CMD} 's|Prerelease = "dev"|Prerelease = ""|' \
		${WRKSRC}/version/version.go

.include <bsd.port.mk>
