# FP_LISTRIK_SEDERHANA
#Final Project Sistem Operasi

import math
import os

print('================================================')
print('|      Program Kalkulator Listrik Sederhana    |')
print('================================================')
print('1. Mencari Tegangan (V)')
print('2. Mencari Arus (I)')
print('3. Mencari Hambatan (R)')
print('4. Mencari Daya (P)')
print('5. Keluar')

def volt() :
    print('================================================')
    print('|        Program Mencari Tengangan (V)         |')
    print('================================================')
    print('1. Jika diketahui Arus (I) dan Hambatan (R)')
    print('2. Jika diketahui Daya (P) dan Arus (I)')
    print('3. Jika diketahui Daya (P) dan Hambatan (R)')

    def i_r() :
        print('================================================')
        i=float(input('Masukkan I : '))
        r=float(input('Masukkan R : '))
        v=i*r
        print('================================================')
        print('V = ',v,'Volt')
        mbalen()

    def p_i() :
        print('================================================')
        p=float(input('Masukkan P : '))
        i=float(input('Masukkan I : '))
        v=p/i
        print('================================================')
        print('V = ',v,'Volt')
        mbalen()

    def p_r() :
        print('================================================')
        p=float(input('Masukkan P : '))
        r=float(input('Masukkan R : '))
        v= math.sqrt(p*r)
        print('================================================')
        print('V = ',v,'Volt')
        mbalen()   

    inputan_1 = int(input('Silahkan Pilih 1-3 : '))
    if inputan_1 == 1 :
        i_r()
    elif inputan_1 == 2 :
        p_i()
    elif inputan_1 == 3 :
        p_r()
    else :
        print('Hanya ada pilihan 1-3!')
        mbalen()

def ampere() :
    print('================================================')
    print('|           Program Mencari Arus (I)           |')
    print('================================================')
    print('1. Jika diketahui Tegangan (V) dan Hambatan (R)')
    print('2. Jika diketahui Daya (P) dan Hambatan (R)')
    print('3. Jika diketahui Daya (P) dan Tegangan (V)')

    def v_r() :
        print('================================================')
        v=float(input('Masukkan V : '))
        r=float(input('Masukkan R : '))
        i=v/r
        print('================================================')
        print('I = ',i,'A')
        mbalen()

    def p_r() :
        print('================================================')
        p=float(input('Masukkan P : '))
        r=float(input('Masukkan R : '))
        i=math.sqrt(p/r)
        print('================================================')
        print('I = ',i,'A')
        mbalen()

    def p_v() :
        print('================================================')
        p=float(input('Masukkan P : '))
        v=float(input('Masukkan V : '))
        i= p/v
        print('================================================')
        print('I = ',i,'A')
        mbalen()

    inputan_2 = int(input('Silahkan Pilih 1-3 : '))
    if inputan_2 == 1 :
        v_r()
    elif inputan_2 == 2 :
        p_r()
    elif inputan_2 == 3 :
        p_v()
    else :
        print('Hanya ada pilihan 1-3!')
        mbalen()

def ohm() :
    print('================================================')
    print('|         Program Mencari Hambatan (R)         |')
    print('================================================')
    print('1. Jika diketahui Tegangan (V) dan Arus (I)')
    print('2. Jika diketahui Daya (P) dan Arus (I)')
    print('3. Jika diketahui Tegangan (V) dan Daya (P)')

    def v_i() :
        print('================================================')
        v=float(input('Masukkan V : '))
        i=float(input('Masukkan I : '))
        r=v/i
        print('================================================')
        print('R = ',r,'Ω')
        mbalen()

    def p_i() :
        print('================================================')
        p=float(input('Masukkan P : '))
        i=float(input('Masukkan I : '))
        r=p/i*i
        print('================================================')
        print('R = ',r,'Ω')
        mbalen()

    def v_p() :
        print('================================================')
        v=float(input('Masukkan V : '))
        p=float(input('Masukkan P : '))
        r=v*v/p
        print('================================================')
        print('R = ',r,'Ω')
        mbalen()

    inputan_3 = int(input('Silahkan Pilih 1-3 : '))
    if inputan_3 == 1 :
        v_i()
    elif inputan_3 == 2 :
        p_i()
    elif inputan_3 == 3 :
        v_p()
    else :
        print('Hanya ada pilihan 1-3!')
        mbalen()

def watt() :
    print('================================================')
    print('|           Program Mencari Daya (P)           |')
    print('================================================')
    print('1. Jika diketahui Tegangan (V) dan Arus (I)')
    print('2. Jika diketahui Arus (I) dan Hambatan (R)')
    print('3. Jika diketahui Tegangan (V) dan Hambatan (R)')

    def v_i() :
        print('================================================')
        v=float(input('Masukkan V : '))
        i=float(input('Masukkan I : '))
        p=v*i
        print('================================================')
        print('P = ',p,'W')
        mbalen()

    def i_r() :
        print('================================================')
        i=float(input('Masukkan I : '))
        r=float(input('Masukkan R : '))
        p=i*i*r
        print('================================================')
        print('P = ',p,'W')
        mbalen()

    def v_r() :
        print('================================================')
        v=float(input('Masukkan V : '))
        r=float(input('Masukkan R : '))
        p=v*v/r
        print('================================================')
        print('P = ',p,'W')
        mbalen()

    inputan_4 = int(input('Silahkan Pilih 1-3 : '))
    if inputan_4 == 1 :
        v_i()
    elif inputan_4 == 2 :
        i_r()
    elif inputan_4 == 3 :
        v_r()
    else :
        print('Hanya ada pilihan 1-3!')
        mbalen()

def mbalen() :
    print('================================================')
    ulang=input('Kembali ke menu awal (y/n) ? : ')
    if ulang == "y" :
        os.system('cls')
        fake()
    elif ulang == "n" :
        print('================================================')
        print('Terimakasih :v')
    else :
        print('Hanya ada y/n !')
        mbalen()

def fake() :
    print('================================================')
    print('|      Program Kalkulator Listrik Sederhana    |')
    print('================================================')
    print('1. Mencari Tegangan (V)')
    print('2. Mencari Arus (I)')
    print('3. Mencari Hambatan (R)')
    print('4. Mencari Daya (P)')
    print('5. Keluar')
    inputan_dalam = int(input('Silahkan Pilih 1-5 : '))
    if inputan_dalam == 1 :
        os.system('cls')
        volt()
    elif inputan_dalam == 2 :
        os.system('cls')
        ampere()
    elif inputan_dalam == 3 :
        os.system('cls')
        ohm()
    elif inputan_dalam == 4 :
        os.system('cls')
        watt()
    elif inputan_dalam == 5 :
        print('================================================')
        print('Terimakasih :v')
    else :
        print('Hanya ada pilihan 1-5!')
        mbalen()
        
inputan_luar = int(input('Silahkan Pilih 1-5 : '))
if inputan_luar == 1 :
    os.system('cls')
    volt()
elif inputan_luar == 2 :
    os.system('cls')
    ampere()
elif inputan_luar == 3 :
    os.system('cls')
    ohm()
elif inputan_luar == 4 :
    os.system('cls')
    watt()
elif inputan_luar == 5 :
    print('================================================')
    print('Terimakasih :v')
else :
    print('Hanya ada pilihan 1-5!')
    mbalen()
