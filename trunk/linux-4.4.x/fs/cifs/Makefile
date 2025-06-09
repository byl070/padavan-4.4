#
# Makefile for Linux CIFS VFS client 
#
obj-$(CONFIG_CIFS) += cifs.o

# 添加 NLS 头文件路径
CFLAGS_cifs.o += -I$(srctree)/fs/nls

cifs-y := cifsfs.o cifssmb.o cifs_debug.o connect.o dir.o file.o inode.o \
	  link.o misc.o netmisc.o smbencrypt.o transport.o asn1.o \
	  cifs_unicode.o nterr.o xattr.o cifsencrypt.o \
	  readdir.o ioctl.o sess.o export.o smb1ops.o winucase.o \
	  cifs_nls.o  # 假设存在 NLS 相关源文件

cifs-$(CONFIG_CIFS_ACL) += cifsacl.o

cifs-$(CONFIG_CIFS_UPCALL) += cifs_spnego.o

cifs-$(CONFIG_CIFS_DFS_UPCALL) += dns_resolve.o cifs_dfs_ref.o

cifs-$(CONFIG_CIFS_FSCACHE) += fscache.o cache.o

cifs-$(CONFIG_CIFS_SMB2) += smb2ops.o smb2maperror.o smb2transport.o \
			    smb2misc.o smb2pdu.o smb2inode.o smb2file.o
