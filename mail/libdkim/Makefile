# Created by: Sergey Skvortsov <skv@protey.ru>
# $FreeBSD$

PORTNAME=	libdkim
PORTVERSION=	1.0.21
CATEGORIES=	mail
MASTER_SITES=	SF

MAINTAINER=	ports@FreeBSD.org
COMMENT=	DKIM (DomainKeys Identified Mail) library

LICENSE=	APACHE20

USES=		uidfix zip ssl
CXXFLAGS+=	-std=gnu++98
USE_LDCONFIG=	YES
SHLIB_MAJOR=	1
PLIST_SUB=	SHLIB_MAJOR="${SHLIB_MAJOR}"

WRKSRC=		${WRKDIR}/${PORTNAME}/src

.include <bsd.port.pre.mk>

.if ${SSL_DEFAULT} == base
BROKEN_FreeBSD_12=	field has incomplete type 'EVP_MD_CTX' (aka 'evp_md_ctx_st')
BROKEN_FreeBSD_13=	field has incomplete type 'EVP_MD_CTX' (aka 'evp_md_ctx_st')
.endif

post-patch:
	${MV} ${WRKSRC}/Makefile ${WRKSRC}/Makefile.prev
	@${SED} -e "s=%%SHLIB_MAJOR%%=${SHLIB_MAJOR}=g" \
		${FILESDIR}/Makefile > ${WRKSRC}/Makefile

.include <bsd.port.post.mk>
