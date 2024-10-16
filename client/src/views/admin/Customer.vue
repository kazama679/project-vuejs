<template>
    <div className="flex">
            <main className="flex-1 p-5 bg-gray-50">
                <div className="bg-white p-6 rounded-lg shadow-lg">
                    <div className="flex justify-between mb-4">
                        <div className='flex gap-4'>
                            {/* Lọc theo vai trò */}
                            <select className="border px-4 py-2 rounded" value={filterRole}>
                                <option value="">Lọc theo vai trò</option>
                                <option value="admin">Admin</option>
                                <option value="users">Users</option>
                            </select>
                            {/* Sắp xếp theo tên */}
                            <select className="border px-4 py-2 rounded" value={sortOrder}>
                                <option value="">Sắp xếp theo tên</option>
                                <option value="az">Sắp xếp từ lớn đến bé</option>
                                <option value="za">Sắp xếp từ bé đến lớn</option>
                            </select>
                        </div>
                    </div>

                    {/* Hiển thị danh sách người dùng */}
                    <table className="table-auto w-full border-collapse border border-gray-200 text-center">
                        <thead className="bg-gray-100">
                            <tr>
                                <th className="px-4 py-2 border">STT</th>
                                <th className="px-4 py-2 border">Avatar</th>
                                <th className="px-4 py-2 border">Tên</th>
                                <th className="px-4 py-2 border">Email</th>
                                <th className="px-4 py-2 border">Phone</th>
                                <th className="px-4 py-2 border">Role</th>
                                <th className="px-4 py-2 border">Date</th>
                                <th className="px-4 py-2 border">Action</th>
                            </tr>
                        </thead>
                        <tbody>
                            <!-- {currentUsers.map((user: User, index: number) => ( -->
                                <tr key={user.id}>
                                    <td className="px-4 py-2 border">{indexOfFirstUser + index + 1}</td>
                                    <td className="px-4 py-2 border">
                                        <div className="flex justify-center items-center">
                                            <img className="h-10 w-10 rounded-full" src='' alt={user.name} />
                                        </div>
                                    </td>
                                    <td className="px-4 py-2 border">{user.name}</td>
                                    <td className="px-4 py-2 border">{user.email}</td>
                                    <td className="px-4 py-2 border">{user.phone}</td>
                                    <td className="px-4 py-2 border">
                                        <button className='text-black px-3 py-1 rounded'>{user.role ? "Admin" : "User"}</button>
                                    </td>
                                    <td className="px-4 py-2 border">{user.created_at}</td>
                                    <td className="px-4 py-2 border">
                                        <div className="flex justify-center gap-2">
                                            <button className="bg-blue-500 text-white px-3 py-1 rounded">View</button>
                                            <!-- {/* Nếu là admin thì không có nút thay đổi trạng thái */} -->
                                            <!-- {user.role ? '' : (
                                                <button onClick={() => changeStatus(user)} className={`${user.status ? "bg-green-500" : "bg-red-500"} text-white px-3 py-1 rounded`}>
                                                    {user.status ? "Đang mở" : "Đang khóa"}
                                                </button> -->
                                            <!-- )} -->
                                        </div>
                                    </td>
                                </tr>
                            <!-- ))} -->
                        </tbody>
                    </table>

                    <!-- {/* Phân trang */}
                    <div className="flex justify-center space-x-2 mt-4">
                        {Array.from({ length: Math.ceil(filteredUsers.length / pageNumber) }, (_, index) => (
                            <button
                                key={index}
                                onClick={() => paginate(index + 1)}
                                className={`px-3 py-1 border rounded ${currentPage === index + 1 ? 'bg-blue-500 text-white' : ''}`}
                            >
                                {index + 1}
                            </button>
                        ))}
                    </div> -->
                </div>
            </main>
        </div>
  </template>
  
  <script setup>
  
  </script>
  
  <style>
  
  </style>