project('BLAS', 'fortran', version: '3.8.0')

sources = [
  'dasum.f',
  'daxpy.f',
  'dcabs1.f',
  'dcopy.f',
  'ddot.f',
  'dgbmv.f',
  'dgemm.f', 'dgemv.f',
  'dger.f',
  'dnrm2.f',
  'drot.f', 'drotg.f', 'drotm.f', 'drotmg.f',
  'dsbmv.f',
  'dscal.f',
  'dsdot.f',
  'dspmv.f',
  'dspr2.f', 'dspr.f',
  'dswap.f',
  'dsymm.f', 'dsymv.f',
  'dsyr2.f', 'dsyr2k.f', 'dsyr.f', 'dsyrk.f',
  'dtbmv.f', 'dtbsv.f',
  'dtpmv.f', 'dtpsv.f',
  'dtrmm.f', 'dtrmv.f', 'dtrsm.f', 'dtrsv.f',
  'idamax.f', 'isamax.f', 'izamax.f',
  'lsame.f',
  'sgemm.f', 'sgemv.f',
  'sger.f',
  'sscal.f',
  'sswap.f',
  'ssyr.f',
  'strsm.f',
  'xerbla.f',
  'zaxpy.f',
  'zcopy.f',
  'zdscal.f',
  'zdotc.f',
  'zdotu.f',
  'zgemm.f', 'zgemv.f',
  'zgeru.f',
  'zher.f',
  'zscal.f',
  'zswap.f',
  'ztrsm.f'
]

libcoinblas = static_library(
  'coinblas', sources,
  install: false)

if add_languages('c', required: false)
  # FIXME other fortran standard libraries
  fortran_lib = meson.get_compiler('c').find_library('gfortran')
endif

coinblas_dep = declare_dependency(link_with: [libcoinblas],
                                  dependencies: [fortran_lib])
