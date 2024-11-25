
require("TSLib")
local sz = require("sz")

local sqlite3 = sz.sqlite3
local ts = require("ts")

function get_seed()
  local L0_2, L1_2, L2_2, L3_2, L4_2, L5_2
  L0_2 = string
  L0_2 = L0_2.format
  L1_2 = "%f"
  L2_2 = socket
  L2_2 = L2_2.gettime
  L2_2, L3_2, L4_2, L5_2 = L2_2()
  L0_2 = L0_2(L1_2, L2_2, L3_2, L4_2, L5_2)
  L1_2 = string
  L1_2 = L1_2.sub
  L2_2 = L0_2
  L3_2 = string
  L3_2 = L3_2.find
  L4_2 = L0_2
  L5_2 = "%."
  L3_2 = L3_2(L4_2, L5_2)
  L3_2 = L3_2 + 1
  L4_2 = -1
  L1_2 = L1_2(L2_2, L3_2, L4_2)
  L2_2 = tonumber
  L3_2 = string
  L3_2 = L3_2.reverse
  L4_2 = L1_2
  L3_2, L4_2, L5_2 = L3_2(L4_2)
  return L2_2(L3_2, L4_2, L5_2)
end
math.randomseed(get_seed())

function 清理沙盒(A0_2)
  local L1_2, L2_2, L3_2, L4_2, L5_2, L6_2, L7_2, L8_2, L9_2, L10_2
  L1_2 = appDataPath
  L2_2 = A0_2
  L1_2 = L1_2(L2_2)
  L2_2 = "/"
  L1_2 = L1_2 .. L2_2
  L2_2 = nLog
  L3_2 = L1_2
  L2_2(L3_2)
  if L1_2 ~= "" then
    L2_2 = L1_2
    L3_2 = "Documents"
    L2_2 = L2_2 .. L3_2
    L3_2 = isFileExist
    L4_2 = L2_2
    L3_2 = L3_2(L4_2)
    if L3_2 then
      L3_2 = os
      L3_2 = L3_2.execute
      L4_2 = "rm -rf "
      L5_2 = L1_2
      L6_2 = "Documents"
      L4_2 = L4_2 .. L5_2 .. L6_2
      L3_2(L4_2)
      L3_2 = os
      L3_2 = L3_2.execute
      L4_2 = "mkdir "
      L5_2 = L1_2
      L6_2 = "Documents"
      L4_2 = L4_2 .. L5_2 .. L6_2
      L3_2(L4_2)
      L3_2 = os
      L3_2 = L3_2.execute
      L4_2 = "chown -R mobile:mobile "
      L5_2 = L1_2
      L6_2 = "Documents"
      L4_2 = L4_2 .. L5_2 .. L6_2
      L3_2(L4_2)
    end
    L3_2 = L1_2
    L4_2 = "Library"
    L3_2 = L3_2 .. L4_2
    L4_2 = isFileExist
    L5_2 = L3_2
    L4_2 = L4_2(L5_2)
    if L4_2 then
      L4_2 = os
      L4_2 = L4_2.execute
      L5_2 = "rm -rf "
      L6_2 = L1_2
      L7_2 = "Library"
      L5_2 = L5_2 .. L6_2 .. L7_2
      L4_2(L5_2)
      L4_2 = os
      L4_2 = L4_2.execute
      L5_2 = "mkdir "
      L6_2 = L1_2
      L7_2 = "Library"
      L5_2 = L5_2 .. L6_2 .. L7_2
      L4_2(L5_2)
      L4_2 = os
      L4_2 = L4_2.execute
      L5_2 = "mkdir "
      L6_2 = L1_2
      L7_2 = "Library/Caches"
      L5_2 = L5_2 .. L6_2 .. L7_2
      L4_2(L5_2)
      L4_2 = os
      L4_2 = L4_2.execute
      L5_2 = "mkdir "
      L6_2 = L1_2
      L7_2 = "Library/Preferences"
      L5_2 = L5_2 .. L6_2 .. L7_2
      L4_2(L5_2)
      L4_2 = os
      L4_2 = L4_2.execute
      L5_2 = "chown -R mobile:mobile "
      L6_2 = L1_2
      L7_2 = "Library"
      L5_2 = L5_2 .. L6_2 .. L7_2
      L4_2(L5_2)
    end
    L4_2 = L1_2
    L5_2 = "tmp"
    L4_2 = L4_2 .. L5_2
    L5_2 = isFileExist
    L6_2 = L4_2
    L5_2 = L5_2(L6_2)
    if L5_2 then
      L5_2 = os
      L5_2 = L5_2.execute
      L6_2 = "rm -rf "
      L7_2 = L1_2
      L8_2 = "tmp"
      L6_2 = L6_2 .. L7_2 .. L8_2
      L5_2(L6_2)
      L5_2 = os
      L5_2 = L5_2.execute
      L6_2 = "mkdir "
      L7_2 = L1_2
      L8_2 = "tmp"
      L6_2 = L6_2 .. L7_2 .. L8_2
      L5_2(L6_2)
      L5_2 = os
      L5_2 = L5_2.execute
      L6_2 = "chown -R mobile:mobile "
      L7_2 = L1_2
      L8_2 = "tmp"
      L6_2 = L6_2 .. L7_2 .. L8_2
      L5_2(L6_2)
    end
    L5_2 = L1_2
    L6_2 = "StoreKit"
    L5_2 = L5_2 .. L6_2
    L6_2 = isFileExist
    L7_2 = L5_2
    L6_2 = L6_2(L7_2)
    if L6_2 then
      L6_2 = os
      L6_2 = L6_2.execute
      L7_2 = "rm -rf "
      L8_2 = L1_2
      L9_2 = "StoreKit"
      L7_2 = L7_2 .. L8_2 .. L9_2
      L6_2(L7_2)
      L6_2 = os
      L6_2 = L6_2.execute
      L7_2 = "mkdir "
      L8_2 = L1_2
      L9_2 = "StoreKit"
      L7_2 = L7_2 .. L8_2 .. L9_2
      L6_2(L7_2)
      L6_2 = os
      L6_2 = L6_2.execute
      L7_2 = "chown -R mobile:mobile "
      L8_2 = L1_2
      L9_2 = "StoreKit"
      L7_2 = L7_2 .. L8_2 .. L9_2
      L6_2(L7_2)
    end
    L6_2 = L1_2
    L7_2 = "SystemData"
    L6_2 = L6_2 .. L7_2
    L7_2 = isFileExist
    L8_2 = L6_2
    L7_2 = L7_2(L8_2)
    if L7_2 then
      L7_2 = os
      L7_2 = L7_2.execute
      L8_2 = "rm -rf "
      L9_2 = L1_2
      L10_2 = "SystemData"
      L8_2 = L8_2 .. L9_2 .. L10_2
      L7_2(L8_2)
      L7_2 = os
      L7_2 = L7_2.execute
      L8_2 = "mkdir "
      L9_2 = L1_2
      L10_2 = "SystemData"
      L8_2 = L8_2 .. L9_2 .. L10_2
      L7_2(L8_2)
      L7_2 = os
      L7_2 = L7_2.execute
      L8_2 = "chown -R mobile:mobile "
      L9_2 = L1_2
      L10_2 = "SystemData"
      L8_2 = L8_2 .. L9_2 .. L10_2
      L7_2(L8_2)
    end
  end
end

function 清理剪切板()
  local L0_2, L1_2, L2_2, L3_2, L4_2, L5_2, L6_2, L7_2, L8_2, L9_2
  L0_2 = "/var/mobile/Library/Caches/com.apple.Pasteboard/"
  L1_2 = ts
  L1_2 = L1_2.hlfs
  L1_2 = L1_2.getFileList
  L2_2 = "/var/mobile/Library/Caches/com.apple.Pasteboard/"
  L1_2 = L1_2(L2_2)
  tableGet = L1_2
  L1_2 = tableGet
  if L1_2 then
    L1_2 = pairs
    L2_2 = tableGet
    L1_2, L2_2, L3_2 = L1_2(L2_2)
    for L4_2, L5_2 in L1_2, L2_2, L3_2 do
      if L5_2 ~= "Schema.plist" then
        L6_2 = os
        L6_2 = L6_2.execute
        L7_2 = "rm -rf "
        L8_2 = L0_2
        L9_2 = L5_2
        L7_2 = L7_2 .. L8_2 .. L9_2
        L6_2(L7_2)
      end
      L6_2 = mSleep
      L7_2 = 100
      L6_2(L7_2)
    end
  end
end

function 清理多余数据()
  local L0_2, L1_2, L2_2, L3_2, L4_2
  L0_2 = isFileExist
  L1_2 = "/var/root/Library/Cookies"
  L0_2 = L0_2(L1_2)
  if L0_2 then
    L0_2 = os
    L0_2 = L0_2.execute
    L1_2 = "rm -rf /var/root/Library/Cookies"
    L0_2(L1_2)
  end
  L0_2 = os
  L0_2 = L0_2.execute
  L1_2 = "rm -rf /var/mobile/Library/Safari"
  L0_2(L1_2)
  L0_2 = os
  L0_2 = L0_2.execute
  L1_2 = "rm -rf /var/mobile/Library/Cookies/Cookies.binarycookies"
  L0_2(L1_2)
  L0_2 = appDataPath
  L1_2 = "com.apple.mobilesafari"
  L0_2 = L0_2(L1_2)
  L1_2 = L0_2
  L2_2 = "Library/Caches"
  L1_2 = L1_2 .. L2_2
  L2_2 = nLog
  L3_2 = "CachesStr:"
  L4_2 = L0_2
  L3_2 = L3_2 .. L4_2
  L2_2(L3_2)
  L2_2 = isFileExist
  L3_2 = L1_2
  L2_2 = L2_2(L3_2)
  if L2_2 then
    L2_2 = os
    L2_2 = L2_2.execute
    L3_2 = "rm -rf "
    L4_2 = L1_2
    L3_2 = L3_2 .. L4_2
    L2_2(L3_2)
  end
  L2_2 = delFile
  L3_2 = "/var/Managed Preferences/mobile/com.apple.mobileserver.plist"
  L2_2(L3_2)
  L2_2 = delFile
  L3_2 = "/var/Managed Preferences/mobile/com.apple.backserver.plist"
  L2_2(L3_2)
  L2_2 = delFile
  L3_2 = "/var/Managed Preferences/mobile/com.apple.mobilePhone.Daemon.plist"
  L2_2(L3_2)
  L2_2 = delFile
  L3_2 = "/Library/Managed Preferences/mobile/com.apple.mobileserver.plist"
  L2_2(L3_2)
  L2_2 = delFile
  L3_2 = "/Library/Managed Preferences/mobile/com.apple.backserver.plist"
  L2_2(L3_2)
  L2_2 = delFile
  L3_2 = "/Library/Managed Preferences/mobile/com.apple.mobilePhone.Daemon.plist"
  L2_2(L3_2)
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "rm -rf /private/var/MobileDevice/ProvisioningProfiles/*"
  L2_2(L3_2)
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "rm -rf /private/var/logs/mediaserverd/com.apple.mediaserverd.plist"
  L2_2(L3_2)
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "rm -rf /private/var/logs/mediaserverd/com.apple.springboardserverd.plist"
  L2_2(L3_2)
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "rm -rf /private/var/logs/mediaserverd/com.apple.backboardserverd.plist"
  L2_2(L3_2)
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "rm -rf /var/mobile/Library/Preferences/com.mobicom.net.plist"
  L2_2(L3_2)
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "rm -rf /var/mobile/Library/Preferences/com.mobicom.net2.plist"
  L2_2(L3_2)
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "rm -rf /private/var/mobile/Library/Preferences/com.apple.wifid.manage.plist"
  L2_2(L3_2)
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "rm -rf /private/var/mobile/Library/Preferences/com.apple.lockdownwd.plist"
  L2_2(L3_2)
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "rm -rf /var/mobile/Containers/Shared/AppGroup/*"
  L2_2(L3_2)
end

function 清理Keychain()
  local L0_2, L1_2, L2_2, L3_2
  L0_2 = sqlite3.open
  L1_2 = "/var/Keychains/keychain-2.db"
  L0_2 = L0_2(L1_2)
  L2_2 = L0_2
  L1_2 = L0_2.exec
  L3_2 = "DELETE FROM genp WHERE agrp!='apple' and agrp!='lockdown-identities' and agrp!='com.apple.apsd'"
  L1_2(L2_2, L3_2)
  L2_2 = L0_2
  L1_2 = L0_2.exec
  L3_2 = "DELETE FROM cert WHERE agrp!='lockdown-identities'"
  L1_2(L2_2, L3_2)
  L2_2 = L0_2
  L1_2 = L0_2.exec
  L3_2 = "DELETE FROM keys WHERE agrp!='lockdown-identities'"
  L1_2(L2_2, L3_2)
  L2_2 = L0_2
  L1_2 = L0_2.exec
  L3_2 = "DELETE FROM inet"
  L1_2(L2_2, L3_2)
  L2_2 = L0_2
  L1_2 = L0_2.exec
  L3_2 = "DELETE FROM sqlite_sequence"
  L1_2(L2_2, L3_2)
  L2_2 = L0_2
  L1_2 = sqlite3.close
  L1_2(L2_2)
  L1_2 = clearAllKeyChains
  L1_2()
  L1_2 = clearPasteboard
  L1_2()
  L1_2 = clearCookies
  L1_2()
end

function 清理safari()
  local L0_2, L1_2, L2_2, L3_2, L4_2, L5_2, L6_2, L7_2, L8_2
  L0_2 = appDataPath
  L1_2 = "com.apple.mobilesafari"
  L0_2 = L0_2(L1_2)
  if L0_2 ~= "" then
    L1_2 = L0_2
    L2_2 = "Library/Cookies/*"
    L1_2 = L1_2 .. L2_2
    L2_2 = os
    L2_2 = L2_2.execute
    L3_2 = "rm -rf "
    L4_2 = L1_2
    L3_2 = L3_2 .. L4_2
    L2_2(L3_2)
    L2_2 = L0_2
    L3_2 = "Library/Caches/*"
    L2_2 = L2_2 .. L3_2
    L3_2 = os
    L3_2 = L3_2.execute
    L4_2 = "rm -rf "
    L5_2 = L2_2
    L4_2 = L4_2 .. L5_2
    L3_2(L4_2)
    L3_2 = L0_2
    L4_2 = "Library/WebKit/*"
    L3_2 = L3_2 .. L4_2
    L4_2 = os
    L4_2 = L4_2.execute
    L5_2 = "rm -rf "
    L6_2 = L3_2
    L5_2 = L5_2 .. L6_2
    L4_2(L5_2)
    L4_2 = L0_2
    L5_2 = "CloudKit/*"
    L4_2 = L4_2 .. L5_2
    L5_2 = os
    L5_2 = L5_2.execute
    L6_2 = "rm -rf "
    L7_2 = L4_2
    L6_2 = L6_2 .. L7_2
    L5_2(L6_2)
    L5_2 = L0_2
    L6_2 = "tmp/*"
    L5_2 = L5_2 .. L6_2
    L6_2 = os
    L6_2 = L6_2.execute
    L7_2 = "rm -rf "
    L8_2 = L5_2
    L7_2 = L7_2 .. L8_2
    L6_2(L7_2)
  end
end

function 随机SSID()
	L1_2 = "ChinaNet-"
	L2_2 = "CandyTime-"
	L3_2 = "TP-LINK-"
	L4_2 = "CMCC-"
	local str = "1234567890QWERTYUIOPASDFGHJKLZXCVBNM"
	local ret =''
	for i = 1, 5 do
		local rchr = math.random(1, string.len(str))
		ret = ret .. string.sub(str, rchr, rchr)
	end
	return "ChinaNet-"..ret
end

function 随机姓氏()
	local str = "123456789"
	local ret =''
	for i = 1, 1 do
		local rchr = math.random(1, string.len(str))
		ret = ret .. string.sub(str, rchr, rchr)
	end
	return ret
end

function 取随机昵称(num)
	local str = "123456789"
	local ret =''
	for i = 1, num do
		local rchr = math.random(1, string.len(str))
		ret = ret .. string.sub(str, rchr, rchr)
	end
	return ret
end

function 取16进制(num)
	local str = "0a1b2c3d4e5f6789"
	local ret =''
	for i = 1, num do
		local rchr = math.random(1, string.len(str))
		ret = ret .. string.sub(str, rchr, rchr)
	end
	return ret
end

function 取16进制偶数()
	local str = "0a2c4e68"
	local rchr = math.random(1, string.len(str))
	return string.sub(str, rchr, rchr)
end

function 取数字(A0_2)
	local str = "";
	math.randomseed(getRndNum()) -- 随机种子初始化真随机数
	for var= 1, A0_2 do
		num = math.random(0, 9)
		str = str..num
	end  
	return str
end

function 取大写字母(num)
	local str = "QWERTYUIOPASDFGHJKLZXCVBNM"
	local ret =''
	for i = 1, num do
		local rchr = math.random(1, string.len(str))
		ret = ret .. string.sub(str, rchr, rchr)
	end
	return ret
end

function 取大小写字母(num)
	local str = "QWERTYUIOPASDFGHJKLZXCVBNMqwertyuiopasdfghjklzxcvbnm"
	local ret =''
	for i = 1, num do
		local rchr = math.random(1, string.len(str))
		ret = ret .. string.sub(str, rchr, rchr)
	end
	return ret
end

function 随机参数(A0_2)
  local L1_2, L2_2, L3_2, L4_2, L5_2, L6_2, L7_2, L8_2, L9_2, L10_2, L11_2, L12_2, L13_2, L14_2, L15_2, L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2
  _ENV["安装检测"] = "true"
  _ENV["随机定位"] = "false"
  _ENV["伪造运营商"] = "0"
  _ENV["伪造真名"] = "0"
  _ENV["伪造URLSchemes"] = "0"
  L1_2 = os
  L1_2 = L1_2.time
  L1_2 = L1_2()
  L2_2 = math
  L2_2 = L2_2.random
  L3_2 = 5184000
  L4_2 = 10368000
  L2_2 = L2_2(L3_2, L4_2)
  L1_2 = L1_2 - L2_2
  BootTime2 = L1_2
  L1_2 = BootTime2
  L1_2 = L1_2 - 28800
  BootTime3 = L1_2
  L1_2 = nLog
  L2_2 = "生成伪装信息"
  L1_2(L2_2)
  L1_2 = {}
  L2_2 = "<?xml version=\"1.0\" encoding=\"UTF-8\"?>"
  L3_2 = "<!DOCTYPE plist PUBLIC \"-//Apple//DTD PLIST 1.0//EN\" \"http://www.apple.com/DTDs/PropertyList-1.0.dtd\">"
  L4_2 = "<plist version=\"1.0\">"
  L5_2 = "<dict>"
  L6_2 = "<key>4GIp</key>"
  L7_2 = "<string>10."
  L8_2 = _ENV["取数字"]
  L9_2 = 2
  L8_2 = L8_2(L9_2)
  L9_2 = "."
  L10_2 = math
  L10_2 = L10_2.random
  L11_2 = 10
  L12_2 = 200
  L10_2 = L10_2(L11_2, L12_2)
  L11_2 = "."
  L12_2 = _ENV["取数字"]
  L13_2 = 2
  L12_2 = L12_2(L13_2)
  L13_2 = "</string>"
  L7_2 = L7_2 .. L8_2 .. L9_2 .. L10_2 .. L11_2 .. L12_2 .. L13_2
  L8_2 = "<key>BSSID</key>"
  L9_2 = "<string>"
  L10_2 = _ENV["取16进制"]
  L11_2 = 1
  L10_2 = L10_2(L11_2)
  L11_2 = _ENV["取16进制偶数"]
  L11_2 = L11_2()
  L12_2 = ":"
  L13_2 = _ENV["取16进制"]
  L14_2 = 2
  L13_2 = L13_2(L14_2)
  L14_2 = ":"
  L15_2 = _ENV["取16进制"]
  L16_2 = 2
  L15_2 = L15_2(L16_2)
  L16_2 = ":"
  L17_2 = _ENV["取16进制"]
  L18_2 = 2
  L17_2 = L17_2(L18_2)
  L18_2 = ":"
  L19_2 = _ENV["取16进制"]
  L20_2 = 2
  L19_2 = L19_2(L20_2)
  L20_2 = ":"
  L21_2 = _ENV["取16进制"]
  L22_2 = 2
  L21_2 = L21_2(L22_2)
  L22_2 = "</string>"
  L9_2 = L9_2 .. L10_2 .. L11_2 .. L12_2 .. L13_2 .. L14_2 .. L15_2 .. L16_2 .. L17_2 .. L18_2 .. L19_2 .. L20_2 .. L21_2 .. L22_2
  L10_2 = "<key>BackCamera-id</key>"
  L11_2 = "<string>"
  L12_2 = string
  L12_2 = L12_2.upper
  L13_2 = _ENV["取16进制"]
  L14_2 = 17
  L13_2, L14_2, L15_2, L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L13_2(L14_2)
  L12_2 = L12_2(L13_2, L14_2, L15_2, L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L13_2 = "</string>"
  L11_2 = L11_2 .. L12_2 .. L13_2
  L12_2 = "<key>BackUpLists</key>"
  L13_2 = "<array/>"
  L14_2 = "<key>Battery</key>"
  L15_2 = "<string>0.99</string>"
  L16_2 = "<key>BatteryChargingOrNot</key>"
  L17_2 = "<false/>"
  L18_2 = "<key>BootTime</key>"
  L19_2 = "<integer>"
  L20_2 = math
  L20_2 = L20_2.random
  L21_2 = 259200
  L22_2 = 864000
  L20_2 = L20_2(L21_2, L22_2)
  L21_2 = "</integer>"
  L19_2 = L19_2 .. L20_2 .. L21_2
  L20_2 = "<key>BootTime2</key>"
  L21_2 = "<string>"
  L22_2 = BootTime2
  L23_2 = "."
  L24_2 = _ENV["取数字"]
  L25_2 = 6
  L24_2 = L24_2(L25_2)
  L25_2 = "</string>"
  L21_2 = L21_2 .. L22_2 .. L23_2 .. L24_2 .. L25_2
  L22_2 = "<key>BootTime3</key>"
  L23_2 = "<date>"
  L24_2 = os
  L24_2 = L24_2.date
  L25_2 = "%Y-%m-%dT%H:%M:%SZ"
  L26_2 = BootTime3
  L24_2 = L24_2(L25_2, L26_2)
  L25_2 = "</date>"
  L23_2 = L23_2 .. L24_2 .. L25_2
  L24_2 = "<key>Bounds</key>"
  L25_2 = "<string>{{0, 0}, {0, 0}}</string>"
  L26_2 = "<key>CarrierName</key>"
  L27_2 = "<string></string>"
  L28_2 = "<key>ChooseApps</key>"
  L29_2 = "<array>"
  L30_2 = "<string>"
  L31_2 = A0_2
  L32_2 = "</string>"
  L30_2 = L30_2 .. L31_2 .. L32_2
  L31_2 = "</array>"
  L32_2 = "<key>CreationDate</key>"
  L33_2 = "<date>"
  L34_2 = os
  L34_2 = L34_2.date
  L35_2 = "%Y-%m-%dT%H:%M:%SZ"
  L36_2 = os
  L36_2 = L36_2.time
  L36_2 = L36_2()
  L36_2 = L36_2 - 28800
  L34_2 = L34_2(L35_2, L36_2)
  L35_2 = "</date>"
  L33_2 = L33_2 .. L34_2 .. L35_2
  L34_2 = "<key>CtRaido</key>"
  L35_2 = "<string>CTRadioAccessTechnologyLTE</string>"
  L36_2 = "<key>DEVICETOKEN</key>"
  L37_2 = "<data>"
  L38_2 = _ENV["取大小写字母"]
  L39_2 = 43
  L38_2 = L38_2(L39_2)
  L39_2 = "</data>"
  L37_2 = L37_2 .. L38_2 .. L39_2
  L38_2 = "<key>DSID</key>"
  L39_2 = "<string>114"
  L40_2 = _ENV["取数字"]
  L41_2 = 8
  L40_2 = L40_2(L41_2)
  L41_2 = "</string>"
  L39_2 = L39_2 .. L40_2 .. L41_2
  L40_2 = "<key>DelWhiteList</key>"
  L41_2 = "<array>"
  L42_2 = "<string>/Documents/111/</string>"
  L43_2 = "<string>/Documents/11/</string>"
  L44_2 = "<string>Documents/32323</string>"
  L45_2 = "<string>/Documents/r1111</string>"
  L46_2 = "<string>/Documents/111112</string>"
  L47_2 = "</array>"
  L48_2 = "<key>DeviceColor</key>"
  L49_2 = "<string></string>"
  L50_2 = "<key>DeviceEnclosureColor</key>"
  L51_2 = "<string></string>"
  L1_2[1] = L2_2
  L1_2[2] = L3_2
  L1_2[3] = L4_2
  L1_2[4] = L5_2
  L1_2[5] = L6_2
  L1_2[6] = L7_2
  L1_2[7] = L8_2
  L1_2[8] = L9_2
  L1_2[9] = L10_2
  L1_2[10] = L11_2
  L1_2[11] = L12_2
  L1_2[12] = L13_2
  L1_2[13] = L14_2
  L1_2[14] = L15_2
  L1_2[15] = L16_2
  L1_2[16] = L17_2
  L1_2[17] = L18_2
  L1_2[18] = L19_2
  L1_2[19] = L20_2
  L1_2[20] = L21_2
  L1_2[21] = L22_2
  L1_2[22] = L23_2
  L1_2[23] = L24_2
  L1_2[24] = L25_2
  L1_2[25] = L26_2
  L1_2[26] = L27_2
  L1_2[27] = L28_2
  L1_2[28] = L29_2
  L1_2[29] = L30_2
  L1_2[30] = L31_2
  L1_2[31] = L32_2
  L1_2[32] = L33_2
  L1_2[33] = L34_2
  L1_2[34] = L35_2
  L1_2[35] = L36_2
  L1_2[36] = L37_2
  L1_2[37] = L38_2
  L1_2[38] = L39_2
  L1_2[39] = L40_2
  L1_2[40] = L41_2
  L1_2[41] = L42_2
  L1_2[42] = L43_2
  L1_2[43] = L44_2
  L1_2[44] = L45_2
  L1_2[45] = L46_2
  L1_2[46] = L47_2
  L1_2[47] = L48_2
  L1_2[48] = L49_2
  L1_2[49] = L50_2
  L1_2[50] = L51_2
  L2_2 = "<key>DieId</key>"
  L3_2 = "<string>"
  L4_2 = _ENV["取数字"]
  L5_2 = 19
  L4_2 = L4_2(L5_2)
  L5_2 = "</string>"
  L3_2 = L3_2 .. L4_2 .. L5_2
  L4_2 = "<key>Freesapce</key>"
  L5_2 = "<real>2"
  L6_2 = _ENV["取数字"]
  L7_2 = 9
  L6_2 = L6_2(L7_2)
  L7_2 = "</real>"
  L5_2 = L5_2 .. L6_2 .. L7_2
  L6_2 = "<key>Freesapce2</key>"
  L7_2 = "<real>6"
  L8_2 = _ENV["取数字"]
  L9_2 = 5
  L8_2 = L8_2(L9_2)
  L9_2 = "."
  L10_2 = _ENV["取数字"]
  L11_2 = 10
  L10_2 = L10_2(L11_2)
  L11_2 = "</real>"
  L7_2 = L7_2 .. L8_2 .. L9_2 .. L10_2 .. L11_2
  L8_2 = "<key>FrontCamera-id</key>"
  L9_2 = "<string>"
  L10_2 = string
  L10_2 = L10_2.upper
  L11_2 = _ENV["取16进制"]
  L12_2 = 17
  L11_2, L12_2, L13_2, L14_2, L15_2, L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L11_2(L12_2)
  L10_2 = L10_2(L11_2, L12_2, L13_2, L14_2, L15_2, L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L11_2 = "</string>"
  L9_2 = L9_2 .. L10_2 .. L11_2
  L10_2 = "<key>GPScheat</key>"
  L11_2 = "<"
  L12_2 = _ENV["随机定位"]
  L13_2 = "/>"
  L11_2 = L11_2 .. L12_2 .. L13_2
  L12_2 = "<key>IDFA</key>"
  L13_2 = "<string>"
  L14_2 = string
  L14_2 = L14_2.upper
  L15_2 = _ENV["取16进制"]
  L16_2 = 8
  L15_2, L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L15_2(L16_2)
  L14_2 = L14_2(L15_2, L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L15_2 = "-"
  L16_2 = string
  L16_2 = L16_2.upper
  L17_2 = _ENV["取16进制"]
  L18_2 = 4
  L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L17_2(L18_2)
  L16_2 = L16_2(L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L17_2 = "-"
  L18_2 = string
  L18_2 = L18_2.upper
  L19_2 = _ENV["取16进制"]
  L20_2 = 4
  L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L19_2(L20_2)
  L18_2 = L18_2(L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L19_2 = "-"
  L20_2 = string
  L20_2 = L20_2.upper
  L21_2 = _ENV["取16进制"]
  L22_2 = 4
  L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L21_2(L22_2)
  L20_2 = L20_2(L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L21_2 = "-"
  L22_2 = string
  L22_2 = L22_2.upper
  L23_2 = _ENV["取16进制"]
  L24_2 = 12
  L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L23_2(L24_2)
  L22_2 = L22_2(L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L23_2 = "</string>"
  L13_2 = L13_2 .. L14_2 .. L15_2 .. L16_2 .. L17_2 .. L18_2 .. L19_2 .. L20_2 .. L21_2 .. L22_2 .. L23_2
  L14_2 = "<key>IDFV</key>"
  L15_2 = "<string>"
  L16_2 = string
  L16_2 = L16_2.upper
  L17_2 = _ENV["取16进制"]
  L18_2 = 8
  L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L17_2(L18_2)
  L16_2 = L16_2(L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L17_2 = "-"
  L18_2 = string
  L18_2 = L18_2.upper
  L19_2 = _ENV["取16进制"]
  L20_2 = 4
  L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L19_2(L20_2)
  L18_2 = L18_2(L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L19_2 = "-"
  L20_2 = string
  L20_2 = L20_2.upper
  L21_2 = _ENV["取16进制"]
  L22_2 = 4
  L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L21_2(L22_2)
  L20_2 = L20_2(L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L21_2 = "-"
  L22_2 = string
  L22_2 = L22_2.upper
  L23_2 = _ENV["取16进制"]
  L24_2 = 4
  L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L23_2(L24_2)
  L22_2 = L22_2(L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L23_2 = "-"
  L24_2 = string
  L24_2 = L24_2.upper
  L25_2 = _ENV["取16进制"]
  L26_2 = 12
  L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L25_2(L26_2)
  L24_2 = L24_2(L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L25_2 = "</string>"
  L15_2 = L15_2 .. L16_2 .. L17_2 .. L18_2 .. L19_2 .. L20_2 .. L21_2 .. L22_2 .. L23_2 .. L24_2 .. L25_2
  L16_2 = "<key>IMEI</key>"
  L17_2 = "<string>35 543607 869965 6</string>"
  L18_2 = "<key>IPhoneOrNot</key>"
  L19_2 = "<integer>0</integer>"
  L20_2 = "<key>IPv6Ip</key>"
  L21_2 = "<string>fe80::"
  L22_2 = _ENV["取16进制"]
  L23_2 = 4
  L22_2 = L22_2(L23_2)
  L23_2 = ":"
  L24_2 = _ENV["取16进制"]
  L25_2 = 4
  L24_2 = L24_2(L25_2)
  L25_2 = ":"
  L26_2 = _ENV["取16进制"]
  L27_2 = 4
  L26_2 = L26_2(L27_2)
  L27_2 = ":"
  L28_2 = _ENV["取16进制"]
  L29_2 = 4
  L28_2 = L28_2(L29_2)
  L29_2 = "</string>"
  L21_2 = L21_2 .. L22_2 .. L23_2 .. L24_2 .. L25_2 .. L26_2 .. L27_2 .. L28_2 .. L29_2
  L22_2 = "<key>Installcheck</key>"
  L23_2 = "<"
  L24_2 = _ENV["安装检测"]
  L25_2 = "/>"
  L23_2 = L23_2 .. L24_2 .. L25_2
  L24_2 = "<key>IsFakeCarrier</key>"
  L25_2 = "<integer>"
  L26_2 = _ENV["伪造运营商"]
  L27_2 = "</integer>"
  L25_2 = L25_2 .. L26_2 .. L27_2
  L26_2 = "<key>IsFakeTrustName</key>"
  L27_2 = "<integer>"
  L28_2 = _ENV["伪造真名"]
  L29_2 = "</integer>"
  L27_2 = L27_2 .. L28_2 .. L29_2
  L28_2 = "<key>IsFakeURLSchemes</key>"
  L29_2 = "<integer>"
  L30_2 = _ENV["伪造URLSchemes"]
  L31_2 = "</integer>"
  L29_2 = L29_2 .. L30_2 .. L31_2
  L30_2 = "<key>IsJailBreakOrNot</key>"
  L31_2 = "<integer>0</integer>"
  L32_2 = "<key>IsWifiOrNot</key>"
  L33_2 = "<integer>1</integer>"
  L34_2 = "<key>KeepCaches</key>"
  L35_2 = "<true/>"
  L36_2 = "<key>LocalIp</key>"
  L37_2 = "<string>192.168."
  L38_2 = math
  L38_2 = L38_2.random
  L39_2 = 1
  L40_2 = 230
  L38_2 = L38_2(L39_2, L40_2)
  L39_2 = "."
  L40_2 = math
  L40_2 = L40_2.random
  L41_2 = 1
  L42_2 = 230
  L40_2 = L40_2(L41_2, L42_2)
  L41_2 = "</string>"
  L37_2 = L37_2 .. L38_2 .. L39_2 .. L40_2 .. L41_2
  L38_2 = "<key>MEID</key>"
  L39_2 = "<string>35543607869965</string>"
  L40_2 = "<key>MNC</key>"
  L41_2 = "<string>03</string>"
  L42_2 = "<key>MacAdress</key>"
  L43_2 = "<string>"
  L44_2 = _ENV["取16进制"]
  L45_2 = 1
  L44_2 = L44_2(L45_2)
  L45_2 = _ENV["取16进制偶数"]
  L45_2 = L45_2()
  L46_2 = ":"
  L47_2 = _ENV["取16进制"]
  L48_2 = 2
  L47_2 = L47_2(L48_2)
  L48_2 = ":"
  L49_2 = _ENV["取16进制"]
  L50_2 = 2
  L49_2 = L49_2(L50_2)
  L50_2 = ":"
  L51_2 = _ENV["取16进制"]
  L52_2 = 2
  L51_2 = L51_2(L52_2)
  L52_2 = ":"
  L53_2 = _ENV["取16进制"]
  L54_2 = 2
  L53_2 = L53_2(L54_2)
  L54_2 = ":"
  L55_2 = _ENV["取16进制"]
  L56_2 = 2
  L55_2 = L55_2(L56_2)
  L56_2 = "</string>"
  L43_2 = L43_2 .. L44_2 .. L45_2 .. L46_2 .. L47_2 .. L48_2 .. L49_2 .. L50_2 .. L51_2 .. L52_2 .. L53_2 .. L54_2 .. L55_2 .. L56_2
  L44_2 = "<key>MobileNetWork</key>"
  L45_2 = "<integer>4</integer>"
  L46_2 = "<key>Model</key>"
  L47_2 = "<string></string>"
  L48_2 = "<key>ModelNumber</key>"
  L49_2 = "<string></string>"
  L50_2 = "<key>Name</key>"
  L51_2 = "<string>"
  L52_2 = _ENV["随机姓氏"]
  L52_2 = L52_2()
  L53_2 = _ENV["取随机昵称"]
  L54_2 = 2
  L53_2 = L53_2(L54_2)
  L54_2 = "</string>"
  L51_2 = L51_2 .. L52_2 .. L53_2 .. L54_2
  L1_2[51] = L2_2
  L1_2[52] = L3_2
  L1_2[53] = L4_2
  L1_2[54] = L5_2
  L1_2[55] = L6_2
  L1_2[56] = L7_2
  L1_2[57] = L8_2
  L1_2[58] = L9_2
  L1_2[59] = L10_2
  L1_2[60] = L11_2
  L1_2[61] = L12_2
  L1_2[62] = L13_2
  L1_2[63] = L14_2
  L1_2[64] = L15_2
  L1_2[65] = L16_2
  L1_2[66] = L17_2
  L1_2[67] = L18_2
  L1_2[68] = L19_2
  L1_2[69] = L20_2
  L1_2[70] = L21_2
  L1_2[71] = L22_2
  L1_2[72] = L23_2
  L1_2[73] = L24_2
  L1_2[74] = L25_2
  L1_2[75] = L26_2
  L1_2[76] = L27_2
  L1_2[77] = L28_2
  L1_2[78] = L29_2
  L1_2[79] = L30_2
  L1_2[80] = L31_2
  L1_2[81] = L32_2
  L1_2[82] = L33_2
  L1_2[83] = L34_2
  L1_2[84] = L35_2
  L1_2[85] = L36_2
  L1_2[86] = L37_2
  L1_2[87] = L38_2
  L1_2[88] = L39_2
  L1_2[89] = L40_2
  L1_2[90] = L41_2
  L1_2[91] = L42_2
  L1_2[92] = L43_2
  L1_2[93] = L44_2
  L1_2[94] = L45_2
  L1_2[95] = L46_2
  L1_2[96] = L47_2
  L1_2[97] = L48_2
  L1_2[98] = L49_2
  L1_2[99] = L50_2
  L1_2[100] = L51_2
  L2_2 = "<key>OPENUDID</key>"
  L3_2 = "<string>"
  L4_2 = _ENV["取16进制"]
  L5_2 = 40
  L4_2 = L4_2(L5_2)
  L5_2 = "</string>"
  L3_2 = L3_2 .. L4_2 .. L5_2
  L4_2 = "<key>OsVersion</key>"
  L5_2 = "<string></string>"
  L6_2 = "<key>RandomModel</key>"
  L7_2 = "<false/>"
  L8_2 = "<key>RandomOSversion</key>"
  L9_2 = "<false/>"
  L10_2 = "<key>RandomResolution</key>"
  L11_2 = "<integer>0</integer>"
  L12_2 = "<key>RandomRetention</key>"
  L13_2 = "<false/>"
  L14_2 = "<key>ReaLIdfa</key>"
  L15_2 = "<false/>"
  L16_2 = "<key>Real14</key>"
  L17_2 = "<string>DNPVJAFMJCLF----356724080998292----35672408099829----b0:19:c6:66:e0:f8----b0:19:c6:66:e0:f7----0x0016381E1068002E----d2aa508be3f5d32e5e8c4c794248b966e5814cdf----F3Y74130BDPJ3QLA----iPhone10,3----MQA52CH/A----d22ap----t8015----15B50----11.1.1 </string>"
  L18_2 = "<key>RealIMEI</key>"
  L19_2 = "<string></string>"
  L20_2 = "<key>RegionInfo</key>"
  L21_2 = "<string></string>"
  L22_2 = "<key>Resolution</key>"
  L23_2 = "<string>{0, 0}</string>"
  L24_2 = "<key>SSID</key>"
  L25_2 = "<string>"
  L26_2 = _ENV["随机SSID"]
  L26_2 = L26_2()
  L27_2 = "</string>"
  L25_2 = L25_2 .. L26_2 .. L27_2
  L26_2 = "<key>Scale</key>"
  L27_2 = "<string></string>"
  L28_2 = "<key>Totalspace</key>"
  L29_2 = "<real>550"
  L30_2 = _ENV["取数字"]
  L31_2 = 8
  L30_2 = L30_2(L31_2)
  L31_2 = "</real>"
  L29_2 = L29_2 .. L30_2 .. L31_2
  L30_2 = "<key>Totalspace2</key>"
  L31_2 = "<real>134"
  L32_2 = _ENV["取数字"]
  L33_2 = 5
  L32_2 = L32_2(L33_2)
  L33_2 = "."
  L34_2 = _ENV["取数字"]
  L35_2 = 8
  L34_2 = L34_2(L35_2)
  L35_2 = "</real>"
  L31_2 = L31_2 .. L32_2 .. L33_2 .. L34_2 .. L35_2
  L32_2 = "<key>UserAgent</key>"
  L33_2 = "<dict/>"
  L34_2 = "<key>accel-offset</key>"
  L35_2 = "<string>1000010000000000d8f1"
  L36_2 = _ENV["取16进制"]
  L37_2 = 20
  L36_2 = L36_2(L37_2)
  L37_2 = "</string>"
  L35_2 = L35_2 .. L36_2 .. L37_2
  L36_2 = "<key>battery-id</key>"
  L37_2 = "<data>"
  L38_2 = _ENV["取大小写字母"]
  L39_2 = 23
  L38_2 = L38_2(L39_2)
  L39_2 = "AAAAAAAABAAABAAAAAQA=</data>"
  L37_2 = L37_2 .. L38_2 .. L39_2
  L38_2 = "<key>chooseSysVersions</key>"
  L39_2 = "<array>"
  L40_2 = "<string>10</string>"
  L41_2 = "</array>"
  L42_2 = "<key>disk-id</key>"
  L43_2 = "<string>00000477d"
  L44_2 = _ENV["取16进制"]
  L45_2 = 23
  L44_2 = L44_2(L45_2)
  L45_2 = "</string>"
  L43_2 = L43_2 .. L44_2 .. L45_2
  L44_2 = "<key>fakeTDdata</key>"
  L45_2 = "<dict>"
  L46_2 = "<key>fakeActiveCoreCount</key>"
  L47_2 = "<string></string>"
  L48_2 = "<key>fakeCoreCount</key>"
  L49_2 = "<string></string>"
  L50_2 = "<key>fakeHResolution</key>"
  L51_2 = "<string></string>"
  L1_2[101] = L2_2
  L1_2[102] = L3_2
  L1_2[103] = L4_2
  L1_2[104] = L5_2
  L1_2[105] = L6_2
  L1_2[106] = L7_2
  L1_2[107] = L8_2
  L1_2[108] = L9_2
  L1_2[109] = L10_2
  L1_2[110] = L11_2
  L1_2[111] = L12_2
  L1_2[112] = L13_2
  L1_2[113] = L14_2
  L1_2[114] = L15_2
  L1_2[115] = L16_2
  L1_2[116] = L17_2
  L1_2[117] = L18_2
  L1_2[118] = L19_2
  L1_2[119] = L20_2
  L1_2[120] = L21_2
  L1_2[121] = L22_2
  L1_2[122] = L23_2
  L1_2[123] = L24_2
  L1_2[124] = L25_2
  L1_2[125] = L26_2
  L1_2[126] = L27_2
  L1_2[127] = L28_2
  L1_2[128] = L29_2
  L1_2[129] = L30_2
  L1_2[130] = L31_2
  L1_2[131] = L32_2
  L1_2[132] = L33_2
  L1_2[133] = L34_2
  L1_2[134] = L35_2
  L1_2[135] = L36_2
  L1_2[136] = L37_2
  L1_2[137] = L38_2
  L1_2[138] = L39_2
  L1_2[139] = L40_2
  L1_2[140] = L41_2
  L1_2[141] = L42_2
  L1_2[142] = L43_2
  L1_2[143] = L44_2
  L1_2[144] = L45_2
  L1_2[145] = L46_2
  L1_2[146] = L47_2
  L1_2[147] = L48_2
  L1_2[148] = L49_2
  L1_2[149] = L50_2
  L1_2[150] = L51_2
  L2_2 = "<key>fakeInstructionSet</key>"
  L3_2 = "<string></string>"
  L4_2 = "<key>fakeModel</key>"
  L5_2 = "<string></string>"
  L6_2 = "<key>fakeRam_size</key>"
  L7_2 = "<string></string>"
  L8_2 = "<key>fakeVResolution</key>"
  L9_2 = "<string></string>"
  L10_2 = "</dict>"
  L11_2 = "<key>kuuid</key>"
  L12_2 = "<string>"
  L13_2 = string
  L13_2 = L13_2.upper
  L14_2 = _ENV["取16进制"]
  L15_2 = 8
  L14_2, L15_2, L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L14_2(L15_2)
  L13_2 = L13_2(L14_2, L15_2, L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L14_2 = "-"
  L15_2 = string
  L15_2 = L15_2.upper
  L16_2 = _ENV["取16进制"]
  L17_2 = 4
  L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L16_2(L17_2)
  L15_2 = L15_2(L16_2, L17_2, L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L16_2 = "-"
  L17_2 = string
  L17_2 = L17_2.upper
  L18_2 = _ENV["取16进制"]
  L19_2 = 4
  L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L18_2(L19_2)
  L17_2 = L17_2(L18_2, L19_2, L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L18_2 = "-"
  L19_2 = string
  L19_2 = L19_2.upper
  L20_2 = _ENV["取16进制"]
  L21_2 = 4
  L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L20_2(L21_2)
  L19_2 = L19_2(L20_2, L21_2, L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L20_2 = "-"
  L21_2 = string
  L21_2 = L21_2.upper
  L22_2 = _ENV["取16进制"]
  L23_2 = 12
  L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L22_2(L23_2)
  L21_2 = L21_2(L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L22_2 = "</string>"
  L12_2 = L12_2 .. L13_2 .. L14_2 .. L15_2 .. L16_2 .. L17_2 .. L18_2 .. L19_2 .. L20_2 .. L21_2 .. L22_2
  L13_2 = "<key>lat</key>"
  L14_2 = "<real>"
  L15_2 = math
  L15_2 = L15_2.random
  L16_2 = 23
  L17_2 = 35
  L15_2 = L15_2(L16_2, L17_2)
  L16_2 = "."
  L17_2 = _ENV["取数字"]
  L18_2 = 14
  L17_2 = L17_2(L18_2)
  L18_2 = "</real>"
  L14_2 = L14_2 .. L15_2 .. L16_2 .. L17_2 .. L18_2
  L15_2 = "<key>lng</key>"
  L16_2 = "<real>"
  L17_2 = math
  L17_2 = L17_2.random
  L18_2 = 100
  L19_2 = 116
  L17_2 = L17_2(L18_2, L19_2)
  L18_2 = "."
  L19_2 = _ENV["取数字"]
  L20_2 = 13
  L19_2 = L19_2(L20_2)
  L20_2 = "</real>"
  L16_2 = L16_2 .. L17_2 .. L18_2 .. L19_2 .. L20_2
  L17_2 = "<key>product-id</key>"
  L18_2 = "<string>"
  L19_2 = _ENV["取16进制"]
  L20_2 = 40
  L19_2 = L19_2(L20_2)
  L20_2 = "</string>"
  L18_2 = L18_2 .. L19_2 .. L20_2
  L19_2 = "<key>serial</key>"
  L20_2 = "<string>F"
  L21_2 = string
  L21_2 = L21_2.upper
  L22_2 = _ENV["取16进制"]
  L23_2 = 11
  L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2 = L22_2(L23_2)
  L21_2 = L21_2(L22_2, L23_2, L24_2, L25_2, L26_2, L27_2, L28_2, L29_2, L30_2, L31_2, L32_2, L33_2, L34_2, L35_2, L36_2, L37_2, L38_2, L39_2, L40_2, L41_2, L42_2, L43_2, L44_2, L45_2, L46_2, L47_2, L48_2, L49_2, L50_2, L51_2, L52_2, L53_2, L54_2, L55_2, L56_2)
  L22_2 = "</string>"
  L20_2 = L20_2 .. L21_2 .. L22_2
  L21_2 = "<key>targetBundleID</key>"
  L22_2 = "<string></string>"
  L23_2 = "<key>udid</key>"
  L24_2 = "<string>"
  L25_2 = _ENV["取16进制"]
  L26_2 = 40
  L25_2 = L25_2(L26_2)
  L26_2 = "</string>"
  L24_2 = L24_2 .. L25_2 .. L26_2
  L25_2 = "<key>wifi-id</key>"
  L26_2 = "<string>"
  L27_2 = _ENV["取16进制"]
  L28_2 = 12
  L27_2 = L27_2(L28_2)
  L28_2 = "</string>"
  L26_2 = L26_2 .. L27_2 .. L28_2
  L27_2 = "</dict>"
  L28_2 = "</plist>"
  L1_2[151] = L2_2
  L1_2[152] = L3_2
  L1_2[153] = L4_2
  L1_2[154] = L5_2
  L1_2[155] = L6_2
  L1_2[156] = L7_2
  L1_2[157] = L8_2
  L1_2[158] = L9_2
  L1_2[159] = L10_2
  L1_2[160] = L11_2
  L1_2[161] = L12_2
  L1_2[162] = L13_2
  L1_2[163] = L14_2
  L1_2[164] = L15_2
  L1_2[165] = L16_2
  L1_2[166] = L17_2
  L1_2[167] = L18_2
  L1_2[168] = L19_2
  L1_2[169] = L20_2
  L1_2[170] = L21_2
  L1_2[171] = L22_2
  L1_2[172] = L23_2
  L1_2[173] = L24_2
  L1_2[174] = L25_2
  L1_2[175] = L26_2
  L1_2[176] = L27_2
  L1_2[177] = L28_2
  L2_2 = ""
  L3_2 = 1
  L4_2 = #L1_2
  L5_2 = 1
  for L6_2 = L3_2, L4_2, L5_2 do
    L7_2 = L2_2
    L8_2 = L1_2[L6_2]
    L2_2 = L7_2 .. L8_2
  end
  L3_2 = io
  L3_2 = L3_2.open
  L4_2 = "/var/mobile/Library/Preferences/IR.plist"
  L5_2 = "wb"
  L3_2 = L3_2(L4_2, L5_2)
  L5_2 = L3_2
  L4_2 = L3_2.write
  L6_2 = L2_2
  L4_2(L5_2, L6_2)
  L5_2 = L3_2
  L4_2 = L3_2.close
  L4_2(L5_2)
  L4_2 = nLog
  L5_2 = "写入完成"
  L4_2(L5_2)
end

function 清理应用(bid)
  local L1_2, L2_2
  closeApp(bid)
  清理沙盒(bid)
  清理剪切板()
  清理Keychain()
  清理safari()
  清理多余数据()
  随机参数(bid)
  toast("清理完成",2)
end

function unzip(A0_2, A1_2)
  local L2_2, L3_2, L4_2, L5_2, L6_2
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "unzip "
  L4_2 = A0_2
  L5_2 = " -d "
  L6_2 = A1_2
  L3_2 = L3_2 .. L4_2 .. L5_2 .. L6_2
  L2_2(L3_2)
end

function copyfile(A0_2, A1_2)
  local L2_2, L3_2, L4_2, L5_2, L6_2
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "cp -rf "
  L4_2 = A0_2
  L5_2 = " "
  L6_2 = A1_2
  L3_2 = L3_2 .. L4_2 .. L5_2 .. L6_2
  L2_2(L3_2)
end

function 读取plist_bid()
   local L0_2, L1_2
  L0_2 = "com.kuaishou.nebula"
  --L0_2="com.jiangjia.gif"  
 return L0_2
end

function 恢复备份(arg1)
  local L0_2, L1_2, L2_2, L3_2, L4_2, L5_2, L6_2, L7_2, L8_2, L9_2, L10_2, L11_2, L12_2
  L0_2 = delFile
  L1_2 = "/private/var/mobile/Media/backUp/result.txt"
  L0_2(L1_2)
  L0_2 = "/private/var/mobile/Media/backUp/hf.zip"
  L1_2 = "/private/var/mobile/Media/backUp/hfDir"
  L2_2 = ts
  L2_2 = L2_2.hlfs
  L2_2 = L2_2.removeDir
  L3_2 = L1_2
  L2_2(L3_2)
  L2_2 = ts
  L2_2 = L2_2.hlfs
  L2_2 = L2_2.makeDir
  L3_2 = L1_2
  L2_2(L3_2)
  L2_2 = isFileExist
  L3_2 = L0_2
  L2_2 = L2_2(L3_2)
  if L2_2 then
    L2_2 = nLog
    L3_2 = "reductionPath->"
    L2_2(L3_2)
    L2_2 = unzip
    L3_2 = L0_2
    L4_2 = L1_2
    L2_2(L3_2, L4_2)
    L2_2 = isFileExist
    L3_2 = "/private/var/mobile/Media/backUp/hfDir/IR.plist"
    L2_2 = L2_2(L3_2)
    if L2_2 then
      bid = arg1
      L2_2 = _ENV["清理应用"]
      L3_2 = bid
      L2_2(L3_2)
      L2_2 = appDataPath
      L3_2 = bid
      L2_2 = L2_2(L3_2)
      L3_2 = "/"
      L2_2 = L2_2 .. L3_2
      L3_2 = "/private/var/mobile/Media/backUp/hfDir/"
      L4_2 = bid
      L5_2 = "/"
      L3_2 = L3_2 .. L4_2 .. L5_2
      L4_2 = nLog
      L5_2 = "bak_path:"
      L6_2 = L3_2
      L5_2 = L5_2 .. L6_2
      L4_2(L5_2)
      L4_2 = copyfile
      L5_2 = "/private/var/mobile/Media/backUp/hfDir/IR.plist"
      L6_2 = "/var/mobile/Library/Preferences/IR.plist"
      L4_2(L5_2, L6_2)
      L4_2 = L3_2
      L5_2 = "Documents"
      L4_2 = L4_2 .. L5_2
      L5_2 = isFileExist
      L6_2 = L4_2
      L5_2 = L5_2(L6_2)
      if L5_2 then
        L5_2 = copyfile
        L6_2 = L4_2
        L7_2 = L2_2
        L5_2(L6_2, L7_2)
      end
      L5_2 = L3_2
      L6_2 = "Library"
      L5_2 = L5_2 .. L6_2
      L6_2 = isFileExist
      L7_2 = L5_2
      L6_2 = L6_2(L7_2)
      if L6_2 then
        L6_2 = copyfile
        L7_2 = L5_2
        L8_2 = L2_2
        L6_2(L7_2, L8_2)
      end
      L6_2 = L3_2
      L7_2 = "tmp"
      L6_2 = L6_2 .. L7_2
      L7_2 = isFileExist
      L8_2 = L6_2
      L7_2 = L7_2(L8_2)
      if L7_2 then
        L7_2 = copyfile
        L8_2 = L6_2
        L9_2 = L2_2
        L7_2(L8_2, L9_2)
      end
      L7_2 = L3_2
      L8_2 = "StoreKit"
      L7_2 = L7_2 .. L8_2
      L8_2 = isFileExist
      L9_2 = L7_2
      L8_2 = L8_2(L9_2)
      if L8_2 then
        L8_2 = copyfile
        L9_2 = L7_2
        L10_2 = L2_2
        L8_2(L9_2, L10_2)
      end
      L8_2 = L3_2
      L9_2 = "SystemData"
      L8_2 = L8_2 .. L9_2
      L9_2 = isFileExist
      L10_2 = L8_2
      L9_2 = L9_2(L10_2)
      if L9_2 then
        L9_2 = copyfile
        L10_2 = L8_2
        L11_2 = L2_2
        L9_2(L10_2, L11_2)
      end
      L9_2 = os
      L9_2 = L9_2.execute
      L10_2 = "chown -R mobile:mobile "
      L11_2 = appDataPath
      L12_2 = bid
      L11_2 = L11_2(L12_2)
      L10_2 = L10_2 .. L11_2
      L9_2(L10_2)
      L9_2 = nLog
      L10_2 = "沙盒恢复完成"
      L9_2(L10_2)
      L9_2 = writeFileString
      L10_2 = "/private/var/mobile/Media/backUp/result.txt"
      L11_2 = "1"
      L12_2 = "a"
      L9_2(L10_2, L11_2, L12_2)
    else
     L2_2 = dialog
      L3_2 = "文件解压失败"
      L4_2 = time
     L2_2(L3_2, L4_2)
    end
  else
    L2_2 = dialog
    L3_2 = "还原文件错误"
    L4_2 = time
    L2_2(L3_2, L4_2)
  end
end
function getList(path)
	local a = io.popen("ls "..path);
	local f = {};
	for l in a:lines() do
		table.insert(f,l)
	end
	a:close()
	return f
end

function 压缩备份(A0_2)
  local L1_2, L2_2, L3_2, L4_2, L5_2, L6_2, L7_2, L8_2, L9_2, L10_2, L11_2
  L1_2 = delFile
  L2_2 = "/private/var/mobile/Media/backUp/result.txt"
  L1_2(L2_2)
  L1_2 = closeApp
  L2_2 = A0_2
  L1_2(L2_2)
  L1_2 = ts
  L1_2 = L1_2.hlfs
  L1_2 = L1_2.isDir
  L2_2 = "/private/var/mobile/Media/backUp"
  L1_2 = L1_2(L2_2)
  if not L1_2 then
    L1_2 = ts
    L1_2 = L1_2.hlfs
    L1_2 = L1_2.makeDir
    L2_2 = "/private/var/mobile/Media/backUp"
    L1_2(L2_2)
    L1_2 = os
    L1_2 = L1_2.execute
    L2_2 = "chown -R mobile:mobile /private/var/mobile/Media/backUp"
    L1_2(L2_2)
  end
  L1_2 = ts
  L1_2 = L1_2.hlfs
  L1_2 = L1_2.makeDir
  L2_2 = "/private/var/mobile/Media/backUp/current"
  L1_2(L2_2)
  L1_2 = os
  L1_2 = L1_2.execute
  L2_2 = "chown -R mobile:mobile /private/var/mobile/Media/backUp/current"
  L1_2(L2_2)
  L1_2 = copyfile
  L2_2 = "/var/mobile/Library/Preferences/IR.plist"
  L3_2 = "/private/var/mobile/Media/backUp/current/IR.plist"
  L1_2(L2_2, L3_2)
  L1_2 = "/private/var/mobile/Media/backUp/current/"
  L2_2 = A0_2
  L3_2 = "/"
  L1_2 = L1_2 .. L2_2 .. L3_2
  L2_2 = ts
  L2_2 = L2_2.hlfs
  L2_2 = L2_2.makeDir
  L3_2 = L1_2
  L2_2(L3_2)
  L2_2 = os
  L2_2 = L2_2.execute
  L3_2 = "chown -R mobile:mobile "
  L4_2 = L1_2
  L3_2 = L3_2 .. L4_2
  L2_2(L3_2)
  L2_2 = appDataPath
  L3_2 = A0_2
  L2_2 = L2_2(L3_2)
  L3_2 = "/"
  L2_2 = L2_2 .. L3_2
  L3_2 = nLog
  L4_2 = L2_2
  L3_2(L4_2)
  L3_2 = L2_2
  L4_2 = "Documents"
  L3_2 = L3_2 .. L4_2
  L4_2 = isFileExist
  L5_2 = L3_2
  L4_2 = L4_2(L5_2)
  if L4_2 then
    L4_2 = copyfile
    L5_2 = L3_2
    L6_2 = L1_2
    L7_2 = "Documents"
    L6_2 = L6_2 .. L7_2
    L4_2(L5_2, L6_2)
  end
  L4_2 = L2_2
  L5_2 = "Library"
  L4_2 = L4_2 .. L5_2
  L5_2 = isFileExist
  L6_2 = L4_2
  L5_2 = L5_2(L6_2)
  if L5_2 then
    L5_2 = copyfile
    L6_2 = L4_2
    L7_2 = L1_2
    L8_2 = "Library"
    L7_2 = L7_2 .. L8_2
    L5_2(L6_2, L7_2)
  end
  L5_2 = L2_2
  L6_2 = "tmp"
  L5_2 = L5_2 .. L6_2
  L6_2 = isFileExist
  L7_2 = L5_2
  L6_2 = L6_2(L7_2)
  if L6_2 then
    L6_2 = copyfile
    L7_2 = L5_2
    L8_2 = L1_2
    L9_2 = "tmp"
    L8_2 = L8_2 .. L9_2
    L6_2(L7_2, L8_2)
  end
  L6_2 = L2_2
  L7_2 = "StoreKit"
  L6_2 = L6_2 .. L7_2
  L7_2 = isFileExist
  L8_2 = L6_2
  L7_2 = L7_2(L8_2)
  if L7_2 then
    L7_2 = copyfile
    L8_2 = L6_2
    L9_2 = L1_2
    L10_2 = "StoreKit"
    L9_2 = L9_2 .. L10_2
    L7_2(L8_2, L9_2)
  end
  L7_2 = L2_2
  L8_2 = "SystemData"
  L7_2 = L7_2 .. L8_2
  L8_2 = isFileExist
  L9_2 = L7_2
  L8_2 = L8_2(L9_2)
  if L8_2 then
    L8_2 = copyfile
    L9_2 = L7_2
    L10_2 = L1_2
    L11_2 = "SystemData"
    L10_2 = L10_2 .. L11_2
    L8_2(L9_2, L10_2)
  end
  L8_2 = os
  L8_2 = L8_2.date
  L9_2 = "%Y年%m月%d日%H点%M分"
  L10_2 = os
  L10_2 = L10_2.time
  L10_2, L11_2 = L10_2()
  L8_2 = L8_2(L9_2, L10_2, L11_2)
  _ENV["日期"] = L8_2
  L8_2 = os
  L8_2 = L8_2.execute
  L9_2 = "cd /private/var/mobile/Media/backUp/current && zip -r /private/var/mobile/Media/backUp/"
  L10_2 = _ENV["日期"]
  L11_2 = ".zip *"
    if   A0_2=="com.jiangjia.gif" or A0_2== "com.kuaishou.nebula"then
		文件第二项= L2_2.."/Documents/imdata"
		local bool,kind = isFileExist(文件第二项)
		if bool then
			if kind then
				dialog("文件jia")
			else
				list = getList(文件第二项) 
				if #list >= 1 then
					dialog("ID.."..list[1],1)
					if   A0_2=="com.jiangjia.gif"  then
						math.randomseed(getRndNum()) -- 随机种子初始化真随机数
						numks = math.random(1000, 9999)
					   L9_2 = L9_2 .."密码-"..numks.. "-正版-老号" .. list[1] .."-" ..  L10_2 .. L11_2
					end
					if   A0_2=="com.kuaishou.nebula"  then
					   L9_2 = L9_2 .. "极速" .. list[1] .."-" ..  L10_2 .. L11_2
					end
				else
					L9_2 = L9_2 .. L10_2 .. L11_2
				end
				
			end
		end
	elseif  A0_2== "com.tencent.mqq"then
		--dialog("OOOO")
		文件第二项= L2_2.."/Library"
		local bool,kind = isFileExist(文件第二项)
		if bool then
			if kind then
				dialog("文件jia")
			else
				list = getList(文件第二项) 
				if #list >= 1 then
					dialog("ID.."..list[1],1)
					L9_2 = L9_2 ..list[1].. "-QQ正版" .."-" ..  L10_2 .. L11_2
				else
					L9_2 = L9_2 .. L10_2 .. L11_2
				end
				
			end
		end
		
	else
		L9_2 = L9_2 .. L10_2 .. L11_2
	end
  L8_2(L9_2)
  L8_2 = nLog
  L9_2 = "备份完成"
  L8_2(L9_2)
  L8_2 = writeFileString
  L9_2 = "/private/var/mobile/Media/backUp/result.txt"
  L10_2 = "1"
  L11_2 = "a"
  L8_2(L9_2, L10_2, L11_2)
end

