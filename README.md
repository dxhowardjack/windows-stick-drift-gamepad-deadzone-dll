# windows-gamepad-off-center-deadzone-dll
This is a dll replacing to fix windows gamepad analog stick off center problem (stick drift) by implementing deadzone.

You may enter windows 'safe mode' and change the dll owner from 'trustedinstaller' to 'Users' to get permission to replace the system dll.
Or just place the patched dll in game execution directory. (it's not working in some case)
(be aware 32 bit is in Windows\SysWOW64 folder, and 64 bit is in Windows\System32.)

=============================================================================
to change deadzone range, you can use tool like 'HxD' to edit my patched file
32 bit:
offset 000234EE 0x68
offset 000234F2 0x98
64 bit:
offset 00028311 0x68
offset 00028316 0x98
patched deadzone range:
0x0........0x68 <deadzone> 0x98........0xff
=============================================================================

The files are win10 solution now.

You can compare them to see how to implement it on other windows version.
Or change the deadzone range if you want.

I don't have XBOX controller, so please let me know whether it works if you meet this requirement:)

Me happy.
